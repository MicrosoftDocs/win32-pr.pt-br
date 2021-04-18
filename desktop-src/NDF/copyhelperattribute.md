---
title: Função CopyHelperAttribute (Ndattributils. h)
description: Cria uma cópia de uma \_ estrutura de atributo auxiliar.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- NDF da função CopyHelperAttribute
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787052"
---
# <a name="copyhelperattribute-function"></a>Função CopyHelperAttribute

A função **CopyHelperAttribute** cria uma cópia de uma estrutura de [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Dest* \[ fora\]
</dt> <dd>

Tipo: **\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _

A estrutura a ser atualizada.

</dd> <dt>

_Source * \[ in\]
</dt> <dd>

Tipo: **const [**helper \_ atributo**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _

A estrutura existente a ser copiada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Os valores de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código de retorno                                                                                   | Descrição                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi realizada com êxito.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um ou mais parâmetros não foram fornecidos corretamente.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória suficiente disponível para concluir esta operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





