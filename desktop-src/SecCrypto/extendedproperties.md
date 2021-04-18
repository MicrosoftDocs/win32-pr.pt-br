---
description: Representa uma coleção de objetos Extended.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Objeto ExtendedProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752126"
---
# <a name="extendedproperties-object"></a>Objeto ExtendedProperties

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar a função de API do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O objeto **ExtendedProperties** representa uma coleção de objetos [**Extended**](extendedproperty.md) . Cada objeto representa uma única propriedade estendida.

## <a name="when-to-use"></a>Quando usar

O objeto **ExtendedProperties** é usado para executar as seguintes tarefas:

-   Adicionar ou remover um objeto [**Extended**](extendedproperty.md) da coleção.
-   Recupere o número de propriedades estendidas na coleção.
-   Recupera um objeto [**estendiproperty**](extendedproperty.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto **ExtendedProperties** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#extendedproperties-object)

### <a name="methods"></a>Métodos

O objeto **ExtendedProperties** tem esses métodos.



| Método                                      | Descrição                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Agrega**](extendedproperties-add.md)       | Adiciona um objeto [**estendiproperty**](extendedproperty.md) à coleção.<br/>      |
| [**Remover**](extendedproperties-remove.md) | Remove um objeto [**estendiproperty**](extendedproperty.md) da coleção.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **ExtendedProperties** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](extendedproperties-count.md)<br/>       | Somente leitura<br/> | Recupera o número de objetos [**Extended**](extendedproperty.md) na coleção.<br/>                                                                                                                      |
| [**Item**](extendedproperties-item.md)<br/>         | Somente leitura<br/> | Recupera um objeto [**estendiproperty**](extendedproperty.md) que representa a propriedade estendida indexada da coleção. Essa é a propriedade padrão.<br/>                                                      |



 

## <a name="remarks"></a>Comentários

O objeto **ExtendedProperties** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
