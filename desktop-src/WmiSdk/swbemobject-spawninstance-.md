---
description: Use o método SpawnInstance \_ do objeto SWbemObject para criar uma nova instância de uma classe.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: SWbemObject.SpawnInstance_ método (Wbemdisp.h)
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
ms.openlocfilehash: 1b465bb53fd031dff397ef0ddf39db39d5d9987f03e037becebcd8dd41a65b87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640036"
---
# <a name="swbemobjectspawninstance_-method"></a>Método SWbemObject.SpawnInstance \_

Use o **método \_ SpawnInstance** do [**objeto SWbemObject**](swbemobject.md) para criar uma nova instância de uma classe. O objeto atual deve ser uma definição de classe obtida do WMI por meio de um método como [**SWbemServices.Get**](swbemservices-get.md) [**ouSWbemServices.ExecQuery**](swbemservices-execquery.md). Em seguida, use essa definição de classe para criar novas instâncias. Crie cada nova instância localmente dentro do processo e chame [**SWbemObject.Put \_**](swbemobject-put-.md) para realmente criar a instância no WMI.

> [!Note]  
> Há suporte para gerar uma instância de uma instância, mas a instância retornada está vazia.

 

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado e deve ser zero se especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedida, essa chamada retornará [**um objeto SWbemObject**](swbemobject.md) que contém uma nova instância da classe .

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método \_ SpawnInstance,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrIncompleteClass** – 2147749920 (0x80041020)
</dt> <dd>

O objeto atual não é uma definição de classe válida e não pode gerar novas instâncias. Ele está incompleto ou não foi registrado no WMI usando [**SWbemObject.Put. \_**](swbemobject-put-.md)

</dd> <dt>

**wbemErr LtdgalOperation** – 2147749918 (0x8004101E)
</dt> <dd>

Retornado se esse método for usado em uma instância em vez de em uma classe .

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Parâmetro inválido foi especificado.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.Put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices.Get**](swbemservices-get.md)
</dt> </dl>

 

 




