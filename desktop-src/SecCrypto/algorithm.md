---
description: Especifica o algoritmo usado para as operações de assinatura, enveloping e criptografia.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Objeto Algorithm (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b52054c170cd8072bde1b742d0446732fa0b89d2be0dfc2efc66d557cdf98fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880156"
---
# <a name="algorithm-object"></a>Objeto de algoritmo

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto **Algorithm** especifica o algoritmo usado para as operações de assinatura, enveloping e criptografia.

## <a name="when-to-use"></a>Quando usar

O objeto de **algoritmo** é usado para executar as seguintes tarefas:

-   Defina ou recupere o algoritmo a ser usado.
-   Definir ou recuperar o comprimento da chave.

> [!Note]  
> O CAPICOM tenta usar o CSP (provedor de serviços de criptografia) padrão do sistema. Se esse CSP não puder fornecer o algoritmo ou o comprimento de chave solicitado, o CAPICOM procura um CSP fornecido pela Microsoft que possa lidar com o algoritmo e o comprimento de chave solicitados, nesta ordem de disponibilidade: provedor criptográfico aprimorado da Microsoft, provedor de criptografia forte da Microsoft, provedor criptográfico base da Microsoft.

 

## <a name="members"></a>Membros

O objeto de **algoritmo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **algoritmo** tem essas propriedades.



| Propriedade                                            | Tipo de acesso           | Descrição                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength da**](algorithm-keylength.md)<br/> | Leitura/gravação<br/> | Define ou recupera o comprimento da chave.<br/>                                                                               |
| [**Nome**](algorithm-name.md)<br/>           | Leitura/gravação<br/> | Define ou recupera o algoritmo usado para as operações de assinatura, enveloping e criptografia. Essa é a propriedade padrão.<br/> |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto de **algoritmo** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| Cabeçalho<br/>                | <dl> <dt>CAPICOM. h</dt> </dl>   |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
