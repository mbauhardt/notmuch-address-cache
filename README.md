notmuch-address-cache(1)                              notmuch-address-cache(1)



NNAAMMEE
       notmuch-address-cache  -  caches  the  result  from notmuch-address and
       search within this cached version.


SSYYNNOOPPSSIISS
       nnoottmmuucchh--aaddddrreessss--ccaacchhee [ _C_O_M_M_A_N_D ] [ _A_R_G ]


DDEESSCCRRIIPPTTIIOONN
       nnoottmmuucchh--aaddddrreessss--ccaacchhee is basically a cache in  front  of  the  _n_o_t_m_u_c_h_-
       _a_d_d_r_e_s_s command.

       notmuch-address-cache caches all sender and recipients you communicated
       with. It expect the notmuch tag ttaagg::aallll on all messages to extract  the
       sender  and  recipients  from there. You can configure notmuch to apply
       the ttaagg::aallll to all messages. This is basically done  if  you  edit  the
       file  _~_/_._n_o_t_m_u_c_h_-_c_o_n_f_i_g, go into section [new] and add the value aallll to
       the key ttaaggss.


CCoommmmaannddss
       hheellpp, ----hheellpp, --hh
              Show help text.

       vveerrssiioonn, ----vveerrssiioonn, --vv
              Show the version.

       rreebbuuiilldd, ----rreebbuuiilldd, --rr [----jjssoonn | ----tteexxtt]
              Uses _n_o_t_m_u_c_h_-_a_d_d_r_e_s_s to find all sender/recipient  you  communi-
              cated  with  and  print them out to the file _~_/_._n_o_t_m_u_c_h_-_a_d_d_r_e_s_s_-
              _c_a_c_h_e_/_a_d_d_r_e_s_s_e_s. The format of the cached addresses  are  stored
              in  json, if you rebuild your cache with option ----jjssoonn. The for-
              mat of the cached addresses are stored in text, if  you  rebuild
              your  cache with option----tteexxtt. Format text is recommended if you
              want to query the cache with mmuutttt. Format json is recommended if
              you want to query the cache with aalloott.

       qquueerryy, ----qquueerryy, --qq
              greps bla bla



version v0.1                       Sep 2017           notmuch-address-cache(1)
