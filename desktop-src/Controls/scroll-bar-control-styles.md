---
title: Estilos de controle da barra de rolagem (WinUser. h)
description: Para criar um controle de barra de rolagem usando a função CreateWindow ou CreateWindowEx, especifique a classe SCROLLBAR, as constantes de estilo de janela apropriadas e uma combinação dos estilos de controle da barra de rolagem a seguir.
ms.assetid: 07195a95-eff8-4a47-926a-9d503fa7b299
topic_type:
- apiref
api_name:
- SBS_BOTTOMALIGN
- SBS_HORZ
- SBS_LEFTALIGN
- SBS_RIGHTALIGN
- SBS_SIZEBOX
- SBS_SIZEBOXBOTTOMRIGHTALIGN
- SBS_SIZEBOXTOPLEFTALIGN
- SBS_SIZEGRIP
- SBS_TOPALIGN
- SBS_VERT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5de721fd4cc44867fca0dbe1b35dcaf58c6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752937"
---
# <a name="scroll-bar-control-styles"></a>Estilos de controle da barra de rolagem

Para criar um controle de barra de rolagem usando a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique a classe ScrollBar, as constantes de estilo de janela apropriadas e uma combinação dos estilos de controle da barra de rolagem a seguir. Alguns dos estilos criam um controle de barra de rolagem que usa uma largura ou altura padrão. No entanto, você sempre deve especificar as coordenadas x e y e as outras dimensões da barra de rolagem ao chamar **CreateWindow** ou **CreateWindowEx**.



| Constante                                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SBS_BOTTOMALIGN"></span><span id="sbs_bottomalign"></span><dl> <dt>**\_BOTTOMALIGN SBS**</dt> </dl>                                     | Alinha a borda inferior da barra de rolagem com a borda inferior do retângulo definido pelos parâmetros *x*, *y*, *NWidth* e *nHeight* da função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . A barra de rolagem tem a altura padrão para as barras de rolagem do sistema. Use esse estilo com o \_ estilo na horizontal do SBS.<br/>                      |
| <span id="SBS_HORZ"></span><span id="sbs_horz"></span><dl> <dt>**\_na horizontal SBS**</dt> </dl>                                                          | Designa uma barra de rolagem horizontal. Se nem o \_ estilo SBS BOTTOMALIGN nem SBS \_ TOPALIGN for especificado, a barra de rolagem terá a altura, a largura e a posição especificados pelos parâmetros *x*, *y*, *nWidth* e *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                      |
| <span id="SBS_LEFTALIGN"></span><span id="sbs_leftalign"></span><dl> <dt>**\_LEFTALIGN SBS**</dt> </dl>                                           | Alinha a borda esquerda da barra de rolagem com a borda esquerda do retângulo definido pelos parâmetros *x*, *y*, *nWidth* e *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). A barra de rolagem tem a largura padrão para as barras de rolagem do sistema. Use esse estilo com o estilo do SBS \_ Vert.<br/>                                    |
| <span id="SBS_RIGHTALIGN"></span><span id="sbs_rightalign"></span><dl> <dt>**\_RIGHTALIGN SBS**</dt> </dl>                                        | Alinha a borda direita da barra de rolagem com a borda direita do retângulo definido pelos parâmetros *x*, *y*, *nWidth* e *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). A barra de rolagem tem a largura padrão para as barras de rolagem do sistema. Use esse estilo com o estilo do SBS \_ Vert.<br/>                                  |
| <span id="SBS_SIZEBOX"></span><span id="sbs_sizebox"></span><dl> <dt>**\_SIZEBOX SBS**</dt> </dl>                                                 | Designa uma caixa de tamanho. Se você não especificar o \_ SIZEBOXBOTTOMRIGHTALIGN SBS nem o \_ estilo SIZEBOXTOPLEFTALIGN do SBS, a caixa Tamanho terá a altura, a largura e a posição especificados pelos parâmetros *x*, *y*, *nWidth* e *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). <br/>                                          |
| <span id="SBS_SIZEBOXBOTTOMRIGHTALIGN"></span><span id="sbs_sizeboxbottomrightalign"></span><dl> <dt>**\_SIZEBOXBOTTOMRIGHTALIGN SBS**</dt> </dl> | Alinha o canto inferior direito da caixa tamanho com o canto inferior direito do retângulo especificado pelos parâmetros *x*, *y*, *nWidth* e *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). A caixa tamanho tem o tamanho padrão para as caixas tamanho do sistema. Use este estilo com os estilos de SIZEGRIP do SBS \_ SIZEBOX ou SBS \_ .<br/> |
| <span id="SBS_SIZEBOXTOPLEFTALIGN"></span><span id="sbs_sizeboxtopleftalign"></span><dl> <dt>**\_SIZEBOXTOPLEFTALIGN SBS**</dt> </dl>             | Alinha o canto superior esquerdo da caixa tamanho com o canto superior esquerdo do retângulo especificado pelos parâmetros *x*, *y*, *nWidth* e *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). A caixa tamanho tem o tamanho padrão para as caixas tamanho do sistema. Use este estilo com os estilos de SIZEGRIP do SBS \_ SIZEBOX ou SBS \_ .<br/>   |
| <span id="SBS_SIZEGRIP"></span><span id="sbs_sizegrip"></span><dl> <dt>**\_SIZEGRIP SBS**</dt> </dl>                                              | O mesmo que o SBS \_ SIZEBOX, mas com uma borda elevada. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="SBS_TOPALIGN"></span><span id="sbs_topalign"></span><dl> <dt>**\_TOPALIGN SBS**</dt> </dl>                                              | Alinha a borda superior da barra de rolagem com a borda superior do retângulo definido pelos parâmetros *x*, *y*, *nWidth* e *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). A barra de rolagem tem a altura padrão para as barras de rolagem do sistema. Use esse estilo com o \_ estilo na horizontal do SBS.<br/>                                     |
| <span id="SBS_VERT"></span><span id="sbs_vert"></span><dl> <dt>**SBS \_ Vert**</dt> </dl>                                                          | Designa uma barra de rolagem vertical. Se você não especificar o \_ RIGHTALIGN SBS nem o \_ estilo LEFTALIGN do SBS, a barra de rolagem terá a altura, a largura e a posição especificados pelos parâmetros *x*, *y*, *nWidth* e *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WinUser. h</dt> </dl> |



 

