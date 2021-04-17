---
title: Estilos estendidos de controle de guia (CommCtrl. h)
description: O controle guia agora dá suporte a estilos estendidos. Esses estilos são manipulados usando as mensagens TCM Extended \_ e TCM \_ setextendedattribute e não devem ser confundidos com estilos de janela estendidos que são passados para CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748714"
---
# <a name="tab-control-extended-styles"></a>Estilos estendidos de controle de guia

O controle guia agora dá suporte a estilos estendidos. Esses estilos são manipulados usando as mensagens TCM Extended e [**TCM \_ setextendedattribute**](tcm-setextendedstyle.md) e não devem ser confundidos com estilos de janela estendidos que são passados para [**\_**](tcm-getextendedstyle.md) [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).



| Constante                                                                                                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TCS \_ ex \_ FLATSEPARATORS**</dt> </dl> | [Versão 4,71](common-control-versions.md). O controle guia desenhará separadores entre os itens da guia. Esse estilo estendido só afeta os controles de guia que têm os [**\_ botões de TCS**](tab-control-styles.md) e os estilos de [**\_ FLATBUTTONS de TCS**](tab-control-styles.md) . Por padrão, a criação do controle guia com o estilo de **\_ FLATBUTTONS de TCS** define esse estilo estendido. Se você não precisar de separadores, deverá remover esse estilo estendido depois de criar o controle.<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TCS \_ ex \_ REGISTERDROP**</dt> </dl>       | [Versão 4,71](common-control-versions.md). O controle guia gera códigos de notificação do [TCN \_ GetObject](tcn-getobject.md) para solicitar um objeto de destino drop quando um objeto é arrastado sobre os itens da guia no controle. O aplicativo deve chamar [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de definir esse estilo. <br/>                                                                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

