---
title: Constantes de TF_SFT_ (Ctfutb. h)
description: O TF \_ SFT \_ \ Constants especifica as configurações de exibição de uma barra de idiomas flutuante.
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796336"
---
# <a name="tf_sft_-constants"></a>Constantes do TF \_ SFT \_ \*

As constantes ** \_ TF \_ \* SFT* _ especificam as configurações de exibição de uma barra de idiomas flutuante.



| Constante/valor                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <dt>_ * TF \_ SFT tudo \_ normal * *</dt> <dt>0x00000001</dt> </dl>                                        | Exiba a barra de idiomas como uma janela flutuante. Essa constante não pode ser combinada com as \_ constantes TF SFT \_ Dock, TF \_ SFT \_ minimizated, TF \_ SFT \_ Hidden ou TF \_ SFT \_ DESKBAND.<br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <dt>**TF \_ \_Encaixe de SFT**</dt> <dt>0x00000002</dt> </dl>                                                          | Encaixe a barra de idiomas em seu próprio painel de tarefas. Essa constante não pode ser combinada com as \_ constantes TF SFT \_ innormal, TF \_ SFT \_ minimizated, TF \_ SFT \_ Hidden ou TF \_ SFT \_ DESKBAND. Disponível apenas no Windows XP.<br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <dt>**TF \_ SFT \_ minimizado**</dt> <dt>0x00000004</dt> </dl>                                           | Exiba a barra de idiomas como um único ícone na bandeja do sistema. Essa constante não pode ser combinada com as \_ constantes TF SFT \_ innormal, TF \_ SFT \_ Dock, TF \_ SFT \_ Hidden ou TF \_ SFT \_ DESKBAND. No Windows XP, use TF \_ SFT \_ DESKBAND em vez disso.<br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <dt>**TF \_ 0x00000008 \_ ocultos de SFT**</dt> <dt></dt> </dl>                                                    | Oculte a barra de idiomas. Essa constante não pode ser combinada com as \_ constantes TF SFT \_ innormal, TF \_ SFT \_ Dock, TF \_ SFT \_ minimizated ou TF \_ SFT \_ DESKBAND.<br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <dt>**TF \_ SFT \_ notransparência**</dt> <dt>0x00000010</dt> </dl>                            | Torne a barra de idiomas opaca.<br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <dt>**TF \_ SFT \_ LOWTRANSPARENCY**</dt> <dt>0x00000020</dt> </dl>                         | Torne a barra de idiomas parcialmente transparente. Disponível somente no Windows 2000 ou posterior.<br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <dt>**TF \_ 0x00000040 de \_ HIGHTRANSPARENCY de SFT**</dt> <dt></dt> </dl>                      | Torne a barra de idiomas altamente transparente. Disponível somente no Windows 2000 ou posterior.<br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <dt>**TF \_ 0x00000080 de \_ Rótulos de SFT**</dt> <dt></dt> </dl>                                                    | Exibir rótulos de texto ao lado dos ícones da barra de idiomas.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <dt>**TF \_ 0x00000100 do SFT \_ NOlabels**</dt> <dt></dt> </dl>                                              | Ocultar rótulos de texto do ícone da barra de idiomas.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <dt>**TF \_ 0x00000200 de \_ EXTRAICONSONMINIMIZED de SFT**</dt> <dt></dt> </dl>       | Exiba os ícones de serviço de texto na barra de tarefas quando a barra de idiomas for minimizada.<br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <dt>**TF \_ 0x00000400 de \_ NOEXTRAICONSONMINIMIZED de SFT**</dt> <dt></dt> </dl> | Oculte os ícones de serviço de texto na barra de tarefas quando a barra de idiomas for minimizada.<br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <dt>**TF \_ 0x00000800 de \_ DESKBAND de SFT**</dt> <dt></dt> </dl>                                              | Encaixe a barra de idiomas na extremidade righthand da barra de tarefas do sistema (imediatamente à esquerda da bandeja do sistema/relógio). Essa constante não pode ser combinada com as \_ constantes TF SFT \_ innormal, TF \_ SFT \_ Dock, TF \_ SFT \_ minimizated ou TF \_ SFT \_ Hidden. Disponível apenas no Windows XP.<br/> |



## <a name="remarks"></a>Comentários

O método [ITfLangBarMgr:: onfloat](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) define o resultado de uma operação **or** lógica em uma ou mais dessas constantes para especificar os atributos do item da barra de idiomas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITfLangBarMgr:: ficar flutuante](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





