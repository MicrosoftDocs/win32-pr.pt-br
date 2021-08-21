---
description: Use o método SpawnDerivedClass do \_ objeto SWbemObject para criar um objeto de classe derivada do objeto atual. O objeto deve ser uma definição de classe que se torna a classe pai do objeto gerado.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: SWbemObject.SpawnDerivedClass_ método (Wbemdisp.h)
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
ms.openlocfilehash: 0ed0a01926c76ecfc4d393a4de8225d7d0c98a9904f113aed18cd1cb5f8ccabb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313790"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>Método SWbemObject.SpawnDerivedClass \_

Use o **método \_ SpawnDerivedClass** do [**objeto SWbemObject**](swbemobject.md) para criar um objeto de classe derivada do objeto atual. O objeto deve ser uma definição de classe que se torna a classe pai do objeto gerado.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Reservado e deve ser 0 (zero) se especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a chamada for bem-sucedida, o [**objeto SWbemObject**](swbemobject.md) conterá o novo objeto de definição de classe. Nenhum objeto retorna quando há um erro.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método \_ SpawnDerivedClass,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErr LtdgalOperation** – 2147749918 (0x8004101E)
</dt> <dd>

O usuário solicitou uma operação ilegal, como gerar uma classe de uma instância.

</dd> <dt>

**wbemErrIncompleteClass** – 2147749920 (0x80041020)
</dt> <dd>

A classe de origem não foi completamente definida ou registrada com o WMI, portanto, uma nova classe derivada não é permitida.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O objeto retornado automaticamente se torna uma subclasse do objeto atual. Esse comportamento não pode ser substituído. Não há nenhum outro método pelo qual você pode criar classes derivadas.

Você não pode criar uma classe derivada de uma classe que seja local para seu próprio processo de cliente. Antes de usar esse método para criar uma classe derivada, você deve criar a classe base. Para criar a classe base, chame [**SWbemObject.Put \_**](swbemobject-put-.md)e recupere a classe base usando [**SWbemServices.Get**](swbemservices-get.md).

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



 

 




