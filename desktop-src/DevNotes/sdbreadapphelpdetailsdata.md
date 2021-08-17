---
Description: Recupera dados do banco de dados de detalhes do Apphelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: Função SdbReadApphelpDetailsData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9e116080ffbfd81cff7dca8674b6be6fc977f3f7b3024bf32779887bde04d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404405"
---
# <a name="sdbreadapphelpdetailsdata-function"></a>Função SdbReadApphelpDetailsData

Recupera dados do banco de dados de detalhes do Apphelp.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdb* \[ Em\]
</dt> <dd>

Um handle para o banco de dados de detalhes apphelp, Apphelp.sdb.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Uma [**estrutura APPHELP \_ DATA.**](apphelp-data.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **TRUE em** caso de êxito **ou FALSE** em caso de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




