---
title: Estilos estendidos de controle de tabulação (CommCtrl.h)
description: O controle de tabulação agora dá suporte a estilos estendidos. Esses estilos são manipulados usando as mensagens TCM \_ GETEXTENDEDSTYLE e TCM SETEXTENDEDSTYLE e não devem ser confundidos com estilos de janela estendidos que são passados para \_ CreateWindowEx.
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
ms.openlocfilehash: bd057a1ced7c2f594b9e4a7a2c67abe963caa270e770eebecd2f36b50f309aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769916"
---
# <a name="tab-control-extended-styles"></a>Estilos estendidos de controle de tabulação

O controle de tabulação agora dá suporte a estilos estendidos. Esses estilos são manipulados usando as mensagens [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) e [**\_ TCM SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) e não devem ser confundidos com estilos de janela estendidos que são passados para [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)



| Constante                                                                                                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TCS \_ EX \_ FLATSEPARATORS**</dt> </dl> | [Versão 4.71.](common-control-versions.md) O controle de tabulação desenhará separadores entre os itens da guia. Esse estilo estendido afeta apenas os controles de guia que têm os estilos [**TCS \_ BUTTONS**](tab-control-styles.md) e [**TCS \_ FLATBUTTONS.**](tab-control-styles.md) Por padrão, a criação do controle de tabulação com o estilo **TCS \_ FLATBUTTONS** define esse estilo estendido. Se você não precisar de separadores, remova esse estilo estendido depois de criar o controle .<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TCS \_ EX \_ REGISTERDROP**</dt> </dl>       | [Versão 4.71.](common-control-versions.md) O controle tab gera códigos de notificação [ \_ TCN GETOBJECT](tcn-getobject.md) para solicitar um objeto de destino de soltar quando um objeto é arrastado sobre os itens de tabulação no controle . O aplicativo deve chamar [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize antes**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) de definir esse estilo. <br/>                                                                                                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

