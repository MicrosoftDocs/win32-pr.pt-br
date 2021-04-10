---
description: Use o \_ método SpawnDerivedClass do objeto SWbemObject para criar um objeto de classe derivada do objeto atual. O objeto deve ser uma definição de classe que se torna a classe pai do objeto gerado.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Método de SWbemObject.SpawnDerivedClass_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165197"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>Método SWbemObject. SpawnDerivedClass \_

Use o **método \_ SpawnDerivedClass** do objeto [**SWbemObject**](swbemobject.md) para criar um objeto de classe derivada do objeto atual. O objeto deve ser uma definição de classe que se torna a classe pai do objeto gerado.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Reservado e deve ser 0 (zero) se especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a chamada for bem-sucedida, o objeto [**SWbemObject**](swbemobject.md) conterá o novo objeto de definição de classe. Nenhum objeto retorna quando há um erro.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **SpawnDerivedClass \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E)
</dt> <dd>

O usuário solicitou uma operação ilegal, como a geração de uma classe de uma instância.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

A classe de origem não foi totalmente definida ou registrada com WMI, portanto, uma nova classe derivada não é permitida.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O objeto retornado automaticamente se torna uma subclasse do objeto atual. Esse comportamento não pode ser substituído. Não há nenhum outro método pelo qual você possa criar classes derivadas.

Você não pode criar uma classe derivada de uma classe que seja local para seu próprio processo de cliente. Antes de usar esse método para criar uma classe derivada, você deve criar a classe base. Para criar a classe base, chame [**SWbemObject. put \_**](swbemobject-put-.md)e recupere a classe base usando [**SWbemServices. Get**](swbemservices-get.md).

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



 

 




