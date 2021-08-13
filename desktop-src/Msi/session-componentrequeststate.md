---
description: A propriedade ComponentRequestState do objeto Session obtém ou solicita uma alteração no estado Ação de uma linha na tabela Componente.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Propriedade Session.ComponentRequestState
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
ms.openlocfilehash: 3cef17ab3a4781f925e92968bd50dfedddd9a0df8e1781a2f209712fc447ef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625232"
---
# <a name="sessioncomponentrequeststate-property"></a>Propriedade Session.ComponentRequestState

A **propriedade ComponentRequestState** do [**objeto Session**](session-object.md) obtém ou solicita uma alteração no estado Ação de uma linha na tabela [Componente](component-table.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Valor da propriedade

Nome da cadeia de caracteres necessária do item de componente, chave primária da tabela Componente.

## <a name="remarks"></a>Comentários



| Estado de seleção        | Valor | Descrição                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Nulo                   | Nulo  | Solicita que nenhuma ação seja tomada para este item.                |
| msiInstallStateAbsent  | 2     | O item deve ser removido.                                         |
| msiInstallStateLocal   | 3     | O item deve ser instalado localmente.                               |
| msiInstallStateSource  | 4     | O item deve ser instalado e executado na mídia de origem.         |
| msiInstallStateDefault | 5     | Se instalado, o item deve ser reinstalado no mesmo estado. |



 

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession é definido como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




