---
description: O método ViewBillboard do objeto UIPreview exibe um tabuleiro autoral usando o controle de host na caixa de diálogo exibida no momento.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Método UIPreview.ViewBillboard
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
ms.openlocfilehash: 9892dc68ae5edb66759e4c19499af56d06fb6efac56b823821cd74c4a28644b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810366"
---
# <a name="uipreviewviewbillboard-method"></a>Método UIPreview.ViewBillboard

O **método ViewBillboard** do objeto [**UIPreview**](uipreview-object.md) exibe um tabuleiro autoral usando o controle de host na caixa de diálogo exibida no momento.

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

Nome necessário do controle que hospeda o oracle, que recebe a marca de diálogo, juntamente com a caixa de diálogo e as chaves primárias da tabela Controlar banco de dados.

</dd> <dt>

*Outdoor* 
</dt> <dd>

O nome necessário do visor a ser exibido usando o controle e a caixa de diálogo atual especificados e a chave primária da tabela de banco de dados do Oracle.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IUIPreview é definido como \_ 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




