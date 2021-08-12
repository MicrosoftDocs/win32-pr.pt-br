---
title: Função CopyRepairInfo (Ndattributils.h)
description: Cria uma cópia de uma estrutura RepairInfo.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- Função CopyRepairInfo NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a054df2b16684840f22295f0c26de6029ef150a97ca8839c98d94713ab030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620431"
---
# <a name="copyrepairinfo-function"></a>Função CopyRepairInfo

A **função CopyRepairInfo** cria uma cópia de uma [**estrutura RepairInfo.**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Dest* \[ out\]
</dt> <dd>

Tipo: **[ **RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\***

A estrutura a ser atualizada.

</dd> <dt>

*Origem* \[ Em\]
</dt> <dd>

Tipo: **const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \***

A estrutura existente a ser copiada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Os valores de retorno possíveis incluem, mas não estão limitados a, o seguinte.



| Código de retorno                                                                                   | Descrição                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi realizada com êxito.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um ou mais parâmetros não foram fornecidos corretamente.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória suficiente disponível para concluir essa operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





