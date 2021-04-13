---
title: Método AppendAttribute INapSoHConstructor (NapProtocol. h)
description: Adiciona um TLV ao final do buffer SoH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Método AppendAttribute NAP
- Método AppendAttribute NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, método AppendAttribute
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499351"
---
# <a name="inapsohconstructorappendattribute-method"></a>Método INapSoHConstructor:: AppendAttribute

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSoHConstructor:: AppendAttribute** adiciona um TLV ao final do buffer soh.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ de no\]
</dt> <dd>

Uma enumeração [**SoHAttributeType**](sohattributetype-enum.md) que indica o tipo de atributo do novo TLV.

</dd> <dt>

*valor* \[ do no\]
</dt> <dd>

Um ponteiro para uma estrutura [**SoHAttributeValue**](sohattributevalue-union.md) que contém o valor para o novo TLV.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O TLV [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) não deve ser adicionado usando essa função. Ele é adicionado como o primeiro TLV de [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md) para pacotes soh recém-criados.

Ao acrescentar um atributo que será consumido pelo sistema NAP, ele não deve ser criptografado ou modificado de nenhuma maneira. Se o HealthEntity requer MACs (verificação de integridade/criptografia) de informações privadas, ele deve ser incluído somente no atributo [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





