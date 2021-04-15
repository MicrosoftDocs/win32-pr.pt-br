---
title: Mensagem de WM_APPCOMMAND (WinUser. h)
description: Notifica uma janela de que o usuário gerou um evento de comando de aplicativo, por exemplo, clicando em um botão de comando do aplicativo usando o mouse ou digitando uma tecla de comando do aplicativo no teclado.
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- Entrada de mouse e teclado de mensagem WM_APPCOMMAND
topic_type:
- apiref
api_name:
- WM_APPCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7f5e71f9a443e12ea56cb8ca23daea148da92aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369502"
---
# <a name="wm_appcommand-message"></a>Mensagem do WM \_ APPCOMMAND

Notifica uma janela de que o usuário gerou um evento de comando de aplicativo, por exemplo, clicando em um botão de comando do aplicativo usando o mouse ou digitando uma tecla de comando do aplicativo no teclado.


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela em que o usuário clicou no botão ou pressionou a chave. Essa pode ser uma janela filho da janela que recebe a mensagem. Para obter mais informações sobre como processar essa mensagem, consulte a seção comentários.

</dd> <dt>

*lParam* 
</dt> <dd>

Use o código a seguir para obter as informações contidas no parâmetro *lParam* .


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



O comando do aplicativo é *cmd*, que pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**APPCOMMAND \_ \_Aumentos de graves**</dt> <dt>20</dt> </dl>                                                                         | Ativar e desativar o aumento de graves.<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**APPCOMMAND \_ \_Baixo baixo**</dt> <dt>19</dt> </dl>                                                                            | Diminuir os graves.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**APPCOMMAND \_ BAIXO \_ de**</dt> <dt>21</dt> </dl>                                                                                  | Aumentar os graves.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**APPCOMMAND \_ NAVEGADOR \_ para trás**</dt> <dt>1</dt> </dl>                                                        | Navegar para trás.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**APPCOMMAND \_ \_Favoritos do navegador**</dt> <dt>6</dt> </dl>                                                     | Abra os favoritos.<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**APPCOMMAND \_ \_Encaminhamento do navegador**</dt> <dt>2</dt> </dl>                                                           | Navegue para a frente.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**APPCOMMAND \_ \_Página inicial do navegador**</dt> <dt>7</dt> </dl>                                                                    | Navegue para a página inicial.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**APPCOMMAND \_ \_Atualização do navegador**</dt> <dt>3</dt> </dl>                                                           | Atualizar página.<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**APPCOMMAND \_ \_Pesquisa de navegador**</dt> <dt>5</dt> </dl>                                                              | Abra a pesquisa.<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**APPCOMMAND \_ \_Parada do navegador**</dt> <dt>4</dt> </dl>                                                                    | Pare o download.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**APPCOMMAND \_ FECHAR**</dt> <dt>31</dt> </dl>                                                                                         | Feche a janela (não o aplicativo).<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**APPCOMMAND \_ COPIAR**</dt> <dt>36</dt> </dl>                                                                                            | Copie a seleção.<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**APPCOMMAND \_ \_Lista de correção**</dt> <dt>45</dt> </dl>                                                          | Exibe a lista de correção quando uma palavra é identificada incorretamente durante a entrada de fala. <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**APPCOMMAND \_ Recortar**</dt> <dt>37</dt> </dl>                                                                                               | Recortar a seleção.<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**APPCOMMAND \_ DITAr \_ ou \_ \_ \_ Ativar/desativar controle de comando**</dt> <dt>43</dt> </dl> | Alterna entre dois modos de entrada de fala: ditado e comando/controle (fornecendo comandos para um aplicativo ou acessando menus). <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**APPCOMMAND \_ Localizar**</dt> <dt>28</dt> </dl>                                                                                            | Abra a caixa de diálogo **Localizar** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**APPCOMMAND \_ Encaminhar \_ email**</dt> <dt>40</dt> </dl>                                                                   | Encaminhe uma mensagem de email.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**APPCOMMAND \_ AJUDA**</dt> <dt>27</dt> </dl>                                                                                            | Abra a caixa de diálogo **ajuda** .<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**APPCOMMAND \_ INICIAR o \_ App1**</dt> <dt>17</dt> </dl>                                                                      | Inicie o App1.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**APPCOMMAND \_ INICIAR \_ App2**</dt> <dt>18</dt> </dl>                                                                      | Inicie App2.<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**APPCOMMAND \_ INICIAR o \_ email**</dt> <dt>15</dt> </dl>                                                                      | Abra o email.<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**APPCOMMAND \_ Mídia de inicialização \_ \_ Select**</dt> <dt>16</dt> </dl>                                             | Vá para o modo de seleção de mídia.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**APPCOMMAND \_ Canal de mídia \_ \_ inoperante**</dt> <dt>52</dt> </dl>                                                | Reduza o valor do canal, por exemplo, para um sintonizador de TV ou rádio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**APPCOMMAND \_ \_Canal \_ de mídia para cima**</dt> <dt>51</dt> </dl>                                                      | Incrementar o valor do canal, por exemplo, para uma TV ou sintonizador de rádio. <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**APPCOMMAND \_ \_ \_ Avanço de mídia rápido**</dt> <dt>49</dt> </dl>                                                | Aumente a velocidade da reprodução do fluxo. Isso pode ser implementado de várias maneiras, por exemplo, usando uma velocidade fixa ou alternando uma série de velocidades crescentes. <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**APPCOMMAND \_ \_NEXTTRACK de mídia**</dt> <dt>11</dt> </dl>                                                          | Vá para a próxima faixa.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**APPCOMMAND \_ \_Pausa de mídia**</dt> <dt>47</dt> </dl>                                                                      | Temporariamente. Se já estiver em pausa, não execute nenhuma ação adicional. Este é um comando de pausa direta que não tem estado. Se houver botões de reprodução e pausa discretos, os aplicativos devem tomar medidas nesse comando, bem como em **\_ pausa de \_ reprodução \_ de mídia APPCOMMAND**. <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**APPCOMMAND \_ \_Reprodução de mídia**</dt> <dt>46</dt> </dl>                                                                         | Comece a jogar na posição atual. Se já estiver em pausa, ele será retomado. Este é um comando de reprodução direta que não tem estado. Se houver botões de **reprodução** e **pausa** discretos, os aplicativos devem tomar medidas nesse comando, bem como em **\_ pausa de \_ reprodução \_ de mídia APPCOMMAND**.<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**APPCOMMAND \_ Reprodução de mídia- \_ \_ pausa**</dt> <dt>14</dt> </dl>                                                      | Reproduzir ou pausar reprodução. Se houver botões de **reprodução** e **pausa** discretos, os aplicativos devem tomar medidas sobre esse comando, bem como **\_ \_ reprodução de mídia APPCOMMAND** e **APPCOMMAND de mídia em \_ \_ pausa**.<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**APPCOMMAND \_ \_PREVIOUSTRACK de mídia**</dt> <dt>12</dt> </dl>                                              | Vá para a faixa anterior.<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**APPCOMMAND \_ \_Registro de mídia**</dt> <dt>48</dt> </dl>                                                                   | Comece a gravar o fluxo atual.<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**APPCOMMAND \_ \_Retrocesso de mídia**</dt> <dt>50</dt> </dl>                                                                   | Retroceder em um fluxo em uma taxa mais alta de velocidade. Isso pode ser implementado de várias maneiras, por exemplo, usando uma velocidade fixa ou alternando uma série de velocidades crescentes. <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**APPCOMMAND \_ \_Parada de mídia**</dt> <dt>13</dt> </dl>                                                                         | Pare a reprodução.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**APPCOMMAND \_ \_ \_ \_ Alternância de MIC on off**</dt> <dt>44</dt> </dl>                                                  | Alterne o microfone.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**APPCOMMAND \_ \_Volume do \_ microfone**</dt> <dt>25</dt> </dl>                                    | Diminuir o volume do microfone.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**APPCOMMAND \_ \_ \_ Mudo de volume do microfone**</dt> <dt>24</dt> </dl>                                    | Ativar mudo do microfone.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**APPCOMMAND \_ \_Volume do \_ microfone**</dt> <dt>26</dt> </dl>                                          | Aumentar o volume do microfone.<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**APPCOMMAND \_ NOVO**</dt> <dt>29</dt> </dl>                                                                                               | Crie uma nova janela.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**APPCOMMAND \_ ABRIR**</dt> <dt>30</dt> </dl>                                                                                            | Abra uma janela.<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**APPCOMMAND \_ COLAR**</dt> <dt>38</dt> </dl>                                                                                         | Colar<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**APPCOMMAND \_ IMPRIMIR**</dt> <dt>33</dt> </dl>                                                                                         | Imprimir documento atual.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**APPCOMMAND \_ Refazer**</dt> <dt>35</dt> </dl>                                                                                            | Refazer a última ação.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**APPCOMMAND \_ RESPONDER \_ ao \_ email**</dt> <dt>39</dt> </dl>                                                               | Responder a uma mensagem de email.<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**APPCOMMAND \_ Economize**</dt> <dt>32</dt> </dl>                                                                                            | Salvar documento atual.<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**APPCOMMAND \_ Enviar \_ email**</dt> <dt>41</dt> </dl>                                                                            | Envie uma mensagem de email.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**APPCOMMAND \_ \_Verificação ortográfica**</dt> <dt>42</dt> </dl>                                                                      | Inicie uma verificação ortográfica.<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**APPCOMMAND \_ AGUDO \_**</dt> <dt>22</dt> </dl>                                                                      | Diminuir os agudos.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**APPCOMMAND \_ AGUDOs \_ de**</dt> <dt>23</dt> </dl>                                                                            | Aumente os agudos.<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**APPCOMMAND \_ DESFAZER**</dt> <dt>34</dt> </dl>                                                                                            | Desfazer a última ação.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ baixo**</dt> <dt>9</dt> </dl>                                                                       | Reduza o volume.<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ mudo**</dt> <dt>8</dt> </dl>                                                                       | Ativar mudo do volume.<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**APPCOMMAND \_ VOLUME \_ up**</dt> <dt>10</dt> </dl>                                                                            | Aumentar o volume.<br/>                                                                                                                                                                                                                                                               |



 

O componente *udevice* indica o dispositivo de entrada que gerou o evento de entrada e pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                 | Significado                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**FAPPCOMMAND \_ CHAVE**</dt> <dt>0</dt> </dl>            | O usuário pressionou uma chave.<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**FAPPCOMMAND \_ MOUSE**</dt> <dt>0x8000</dt> </dl> | O usuário clicou em um botão do mouse.<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**FAPPCOMMAND \_ OEM**</dt> <dt>0x1000</dt> </dl>       | Uma fonte de hardware não identificada gerou o evento. Pode ser um mouse ou um evento de teclado.<br/> |



 

O componente *dwKeys* indica se várias chaves virtuais estão inativas e pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                               | Significado                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0X0008</dt> de controle </dl>    | A tecla CTRL está inoperante.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | O botão esquerdo do mouse está inativo.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | O botão do meio do mouse está inativo.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | O botão direito do mouse está inativo.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | A tecla SHIFT está inoperante.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | O primeiro botão X está inoperante.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | O segundo botão X está inoperante.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar **true**. Para obter mais informações sobre como processar o valor de retorno, consulte a seção comentários.

## <a name="remarks"></a>Comentários

O [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gera a mensagem do **WM \_ APPCOMMAND** ao processar a mensagem do WM [**\_ XBUTTONUP**](wm-xbuttonup.md) ou do [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md) ou quando o usuário digita uma chave de comando do aplicativo.

Se uma janela filho não processar essa mensagem e, em vez disso, chamar [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), o **DefWindowProc** enviará a mensagem à sua janela pai. Se uma janela de nível superior não processar essa mensagem e, em vez disso, chamar **DefWindowProc**, **DefWindowProc** chamará um gancho de shell com o código de gancho igual a **HSHELL \_ APPCOMMAND**.

Para obter as coordenadas do cursor se a mensagem tiver sido gerada por um clique do mouse, o aplicativo poderá chamar [**GetMessagePos**](/windows/desktop/api/winuser/nf-winuser-getmessagepos). Um aplicativo pode testar se a mensagem foi gerada pelo mouse verificando se *lParam* contém o **\_ mouse FAPPCOMMAND**.

Ao contrário de outras mensagens do Windows, um aplicativo deve retornar **true** desta mensagem se a processar. Isso permitirá que o software que simula essa mensagem em sistemas Windows anteriores ao Windows 2000 determine se o procedimento de janela processou a mensagem ou chamou [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processá-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OBTER \_ \_ lParam APPCOMMAND**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**OBTER \_ lParam do dispositivo \_**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**OBTER \_ \_ lParam KeyState**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**XBUTTONUP do WM \_**](wm-xbuttonup.md)
</dt> <dt>

[**NCXBUTTONUP do WM \_**](wm-ncxbuttonup.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> </dl>

 

