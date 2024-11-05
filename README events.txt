
negotiation event overview:

basics: event.100 is a hidden event so I can keep the FROM-chain going. This is my band-aid solution because I tried working with dynamic flags but couldn't get it to work.
	event.101 clears all flags

major initiates via diplo action

event.1 to minor (I.accept/II.refuse/III.negotiate) 

I. accept
event.2 to major (END)

II.refuse
event.3 to major (I.get wargoal/II.do nothing)
	I.wargoal
		event.4 to minor (information)
	II.do nothing
		event.5 to minor (information)

III.negotiate
event.20 to minor (adm/dip/mil)
	event.21/22/23: lists with 6 options each sorted by adm/dip/mil

event.6/7/8 (adm/dip/mil variants) to major (I.accept/II.offer half/III.offer alternative/IV.demand surrender/V.leave)
I. accept
create subject + event.9 to minor (END)

II.offer half
event.10 to minor (I.accept/II.refuse)
	I.accept
		event.30 (sorts for adm/dip/mil) -> event.11/12/13 to major
			major gets debuffs and subject	(END)
	II.refuse
		event.3 (END)

III.offer alternative (from same category)
event.24/25/26
	event.14/15/16 to minor (I.accept/II.refuse)
		I.accept
			minor gets some dev
				event.40 -> event.42/43/44 (sorted by dev of the minor) 		
					major vassalises minor (END)
<		II.refuse
			event.3 to major (like earlier - END)

IV.demand surrender
event.17 to minor (I.accept/II.refuse)
	I.accept
		event.2 to major (END)
	II.refuse
		event.3 to major (like earlier - END)

V.leave
event.18 to minor (END)
	