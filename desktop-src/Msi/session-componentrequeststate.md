---
description: A propriedade ComponentRequestState do objeto Session Obtém ou solicita uma alteração no estado de ação de uma linha na tabela de componentes.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Propriedade Session. ComponentRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766386"
---
# <a name="sessioncomponentrequeststate-property"></a>Propriedade Session. ComponentRequestState

A propriedade **ComponentRequestState** do objeto [**Session**](session-object.md) Obtém ou solicita uma alteração no estado de ação de uma linha na [tabela de componentes](component-table.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Valor da propriedade

Nome de cadeia de caracteres necessário do item de componente, chave primária da tabela de componentes.

## <a name="remarks"></a>Comentários



| Estado da seleção        | Valor | Descrição                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Nulo                   | Nulo  | Solicita que nenhuma ação seja executada para este item.                |
| msiInstallStateAbsent  | 2     | O item deve ser removido.                                         |
| msiInstallStateLocal   | 3     | O item deve ser instalado localmente.                               |
| msiInstallStateSource  | 4     | O item deve ser instalado e executado a partir da mídia de origem.         |
| msiInstallStateDefault | 5     | Se instalado, o item será reinstalado no mesmo estado. |



 

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




