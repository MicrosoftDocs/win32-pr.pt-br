---
description: Use o \_ método SpawnInstance do objeto SWbemObject para criar uma nova instância de uma classe.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Método de SWbemObject.SpawnInstance_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171788"
---
# <a name="swbemobjectspawninstance_-method"></a>Método SWbemObject. SpawnInstance \_

Use o **método \_ SpawnInstance** do objeto [**SWbemObject**](swbemobject.md) para criar uma nova instância de uma classe. O objeto atual deve ser uma definição de classe obtida do WMI por meio de um método como [**SWbemServices. Get**](swbemservices-get.md) ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md). Em seguida, use essa definição de classe para criar novas instâncias. Crie cada nova instância localmente no processo e chame [**SWbemObject. put \_**](swbemobject-put-.md) para realmente criar a instância no WMI.

> [!Note]  
> Há suporte para a geração de uma instância de uma instância, mas a instância retornada está vazia.

 

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado e deve ser zero se especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedida, essa chamada retornará um objeto [**SWbemObject**](swbemobject.md) que contém uma nova instância da classe.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **SpawnInstance \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

O objeto atual não é uma definição de classe válida e não pode gerar novas instâncias. Ele está incompleto ou não foi registrado com o WMI usando [**SWbemObject. put \_**](swbemobject-put-.md).

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E)
</dt> <dd>

Retornado se esse método for usado em uma instância em vez de uma classe.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Foi especificado um parâmetro inválido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject. put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices. Get**](swbemservices-get.md)
</dt> </dl>

 

 




