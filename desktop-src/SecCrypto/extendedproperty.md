---
description: Representa uma propriedade estendida da Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: Objeto Extended
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778686"
---
# <a name="extendedproperty-object"></a>Objeto Extended

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O objeto **Extended** representa uma propriedade estendida da Microsoft.

## <a name="when-to-use"></a>Quando usar

O objeto **Extended** é usado para executar as seguintes tarefas:

-   Defina ou recupere o tipo da propriedade estendida.
-   Defina ou recupere o tipo de codificação usado para codificar a propriedade estendida.

## <a name="members"></a>Membros

O objeto **Extended** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **Extended** tem essas propriedades.



| Propriedade                                             | Tipo de acesso           | Descrição                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PropID**](extendedproperty-propid.md)<br/> | Leitura/gravação<br/> | Um valor da enumeração [**\_ Propid de CAPICOM**](capicom-propid.md) que define ou recupera o tipo de propriedade estendida.<br/> Essa é a propriedade padrão.<br/> |
| [**Valor**](extendedproperty-value.md)<br/>   | Leitura/gravação<br/> | Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que define ou recupera os dados da propriedade estendida.<br/>                              |



 

## <a name="remarks"></a>Comentários

O objeto **Extended** é usado pela coleção [**ExtendedProperties**](extendedproperties.md) .

O objeto **Extended** pode ser criado e não é seguro para scripts. O ProgID para o objeto **Extended** é CAPICOM. Extended. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
