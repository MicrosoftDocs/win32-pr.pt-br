---
description: Representa uma coleção de objetos de extensão.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Objeto de extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e484de5b4266c5a2458d15365d44a3461a7d1d0589e22391b1afd66e437e02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006834"
---
# <a name="extensions-object"></a>Objeto de extensões

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **Extensions** representa uma coleção de objetos de [**extensão**](extension.md) . Cada objeto de [**extensão**](extension.md) representa uma única extensão de certificado.

## <a name="when-to-use"></a>Quando usar

O objeto de **extensões** é usado para executar as seguintes tarefas:

-   Recupere o número de extensões de certificado na coleção.
-   Recupere um objeto de [**extensão**](extension.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto de **extensões** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **extensões** tem essas propriedades.



| Propriedade                                           | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. essa propriedade é oculta no Visual Basic scripting Edition (VBScript).<br/> |
| [**Contagem**](extensions-count.md)<br/>       | Somente leitura<br/> | Recupera o número de objetos de [**extensão**](extension.md) na coleção.<br/>                                                                                                                                    |
| [**Item**](extensions-item.md)<br/>         | Somente leitura<br/> | Recupera o objeto de [**extensão**](extension.md) que representa a extensão de certificado indexado da coleção. Essa é a propriedade padrão.<br/>                                                               |



 

## <a name="remarks"></a>Comentários

O objeto **Extensions** é retornado pelo método [**Certificate. Extensions**](certificate-extensions.md) .

Não é possível criar o objeto de **extensões** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
