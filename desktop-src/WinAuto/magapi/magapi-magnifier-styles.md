---
title: Estilos da lupa
description: Este tópico descreve os estilos usados com o controle lupa.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369633"
---
# <a name="magnifier-styles"></a>Estilos da lupa

Este tópico descreve os estilos usados com o controle lupa. Para criar um controle de lupa, use a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) e especifique a classe de janela WC_MAGNIFIER, juntamente com uma combinação dos estilos de lupa a seguir.

| Requisito | Valor |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Corta a área da janela da lupa que circunda o cursor do sistema. Esse estilo permite que o usuário veja o conteúdo da tela que está atrás da janela da lupa. |
| MS_INVERTCOLORS 0x0004L | Exibe o conteúdo da tela ampliada usando cores invertidas. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Exibe o cursor do sistema ampliado junto com o conteúdo da tela ampliada. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Ampliação. h</dt> </dl> |

## <a name="see-also"></a>Consulte também

[Constantes](entry-magapi-constants.md)
