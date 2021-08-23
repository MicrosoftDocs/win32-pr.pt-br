---
title: Sinalizadores de criação de lista de imagens (Shlobj.h)
description: O conjunto de sinalizadores de bits que especifica o tipo de lista de imagens a ser criado. Esse parâmetro pode ser uma combinação dos valores a seguir, mas pode incluir apenas um dos valores color \_ ILC. Usado por ImageList \_ Create e IImageList2 Initialize.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1197604750e5da9248200b2dbcf37e53611d83842a401aafc3d2ded70c9179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958685"
---
# <a name="image-list-creation-flags"></a>Sinalizadores de criação de lista de imagens

O conjunto de sinalizadores de bits que especifica o tipo de lista de imagens a ser criado. Esse parâmetro pode ser uma combinação dos valores a seguir, mas pode incluir apenas um dos valores color \_ ILC. Usado por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).



| Constante/valor                                                                                                                                                                                                                                     | Descrição                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**ILC \_ MASK**</dt> <dt>0x00000001</dt> </dl>                                     | Use uma máscara. A lista de imagens contém dois bitmaps, um dos quais é um bitmap monocromático usado como uma máscara. Se esse valor não estiver incluído, a lista de imagens conterá apenas um bitmap.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**ILC \_ Color**</dt> <dt>0x00000000</dt> </dl>                                  | Use o comportamento padrão se nenhum dos outros sinalizadores COLORx ILC \_ for especificado. Normalmente, o padrão é ILC COLOR4, mas para drivers de exibição mais \_ antigos, o padrão é ILC \_ COLORDDB.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**ILC \_ ColorDDB**</dt> <dt>0x000000FE</dt> </dl>                         | Use um bitmap dependente do dispositivo.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt> </dl>                               | Use uma seção DIB (bitmap independente de dispositivo) de 4 bits (16 cores) como o bitmap da lista de imagens.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt> </dl>                               | Use uma seção DIB de 8 bits. As cores usadas para a tabela de cores são as mesmas cores que a paleta de semitonas.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt> </dl>                            | Use uma seção DIB de 16 bits (32/64k-color).<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt> </dl>                            | Use uma seção DIB de 24 bits.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt> </dl>                            | Use uma seção DIB de 32 bits.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**ILC \_ PALETA**</dt> <dt>0x00000800</dt> </dl>                            | Não implementado.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**ILC \_ MIRROR**</dt> <dt>0x00002000</dt> </dl>                               | Espelhar os ícones contidos, se o processo for espelhado<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**ILC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt> </dl>          | Faz com que o código de espelhamento espelhar cada item ao inserir um conjunto de imagens, em comparação com a faixa inteira.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**ILC \_ ORIGINALSIZE**</dt> <dt>0x00010000</dt> </dl>             | **Windows Vista e posterior.** Imagelist deve aceitar imagens menores do que definir e aplicar o tamanho original com base na imagem adicionada.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**ILC \_ HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista e posterior.** Reservado.<br/>                                                                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 





