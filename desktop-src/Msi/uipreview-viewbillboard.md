---
description: O método ViewBillboard do objeto UIPreview exibe um mural criado usando o controle de host na caixa de diálogo exibida no momento.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Método UIPreview. ViewBillboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750591"
---
# <a name="uipreviewviewbillboard-method"></a>Método UIPreview. ViewBillboard

O método **ViewBillboard** do objeto [**UIPreview**](uipreview-object.md) exibe um mural criado usando o controle de host na caixa de diálogo exibida no momento.

## <a name="syntax"></a>Sintaxe


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*control* 
</dt> <dd>

Nome necessário do controle que hospeda o mural, diferencia maiúsculas de minúsculas, juntamente com a caixa de diálogo e as chaves primárias da tabela do banco de dados de controle.

</dd> <dt>

*mensagem* 
</dt> <dd>

Nome necessário do mural a ser exibido usando o controle especificado e a caixa de diálogo atual e a chave primária da tabela do banco de dados do mural.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview é definido como 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




