---
title: ncacn_at_dsp atributo
description: A \_ \_ palavra-chave ncacn at DSP identifica o DSP do AppleTalk como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb021f9212f1034f0b3c235ad77d9ad270325af914887252494316f9ae1c41b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642767"
---
# <a name="ncacn_at_dsp-attribute"></a>ncacn \_ no \_ atributo DSP

A palavra-chave **ncacn \_ at \_ DSP** identifica o DSP do AppleTalk como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome da porta* 
</dt> <dd>

Especifica uma cadeia de caracteres de até 22 bytes de comprimento.

</dd> </dl>

## <a name="remarks"></a>Comentários

A sintaxe da cadeia de caracteres de porta do DSP do AppleTalk, como todas as cadeias de porta, é definida pela implementação do transporte e é independente da especificação de IDL. O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta. Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**extremidade**](endpoint.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Associação de cadeia de caracteres**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 