---
title: Valores de WTNCA (uxtheme. h)
description: Especifica os sinalizadores que modificam os atributos de estilo visual da janela. Use uma combinação de bits ou bit-a-bit dos valores a seguir.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5528e26b7dc24a744affad84c8fd1fe74607ed1af56e20651fd43723cdbbff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059286"
---
# <a name="wtnca-values"></a>Valores de WTNCA

Especifica os sinalizadores que modificam os atributos de estilo visual da janela. Use uma combinação de bits ou bit-a-bit dos valores a seguir.



| Constante/valor                                                                                                                                                                                                                                  | Descrição                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <dt>**WTNCA \_ NODRAWCAPTION**</dt> <dt>0x00000001</dt> </dl> | Impede que a legenda da janela seja desenhada.<br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <dt>**WTNCA \_ NODRAWICON**</dt> <dt>0x00000002</dt> </dl>          | Impede que o ícone do sistema seja desenhado.<br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <dt>**WTNCA \_ NOSYSMENU**</dt> <dt>0x00000004</dt> </dl>             | Impede que o menu de ícone do sistema apareça.<br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <dt>**WTNCA \_ NOMIRRORHELP**</dt> <dt>0x00000008</dt> </dl>    | Impede o espelhamento do ponto de interrogação, mesmo no layout da direita para a esquerda (RTL).<br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <dt>**WTNCA \_ VALIDBITS**</dt> </dl>                                                                             | Uma máscara que contém todos os bits válidos.<br/>                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Uxtheme. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**opções de WTA \_**](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[**SetWindowThemeNonClientAttributes**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





