---
description: Objeto Certificates-representa uma coleção de objetos de certificado.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Objeto de certificados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8efb9221f39b8544eabe8f6c00d21f6cfdf20c14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098384"
---
# <a name="certificates-object"></a>Objeto de certificados

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **Certificates** representa uma coleção de objetos de [**certificado**](certificate.md) . Cada objeto de [**certificado**](certificate.md) representa um único [*certificado digital*](../secgloss/d-gly.md).

O objeto **Certificates** expõe as seguintes interfaces:

-   **ICertificates2**: introduzido no capicom 2,0.
-   **ICertificates**: introduzido no capicom 1,0.

## <a name="when-to-use"></a>Quando usar

O objeto **Certificates** é usado para executar as seguintes tarefas:

-   Adicionar ou remover um objeto de [**certificado**](certificate.md) de ou para a coleção.
-   Gere um subconjunto da coleção encontrando um conjunto de certificados ou exibindo uma caixa de diálogo para selecionar os certificados.
-   Limpe todos os objetos de [**certificado**](certificate.md) da coleção.
-   Recupere o número de certificados na coleção.
-   Recupere um objeto de [**certificado**](certificate.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto **Certificates** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Certificates** tem esses métodos.



| Método                                | Descrição                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Agrega**](certificates-add.md)       | Adiciona um objeto de [**certificado**](certificate.md) à coleção.<br/> (Herdado de **CertificatesICertificates2**)                                        |
| [**Limpar**](certificates-clear.md)   | Remove todos os objetos de [**certificado**](certificate.md) da coleção.<br/> (Herdado de **CertificatesICertificates2**)                                |
| [**Localizar**](certificates-find.md)     | Retorna um objeto **Certificates** que contém todos os certificados que correspondem aos critérios de pesquisa especificados.<br/> (Herdado de **CertificatesICertificates2**) |
| [**Remover**](certificates-remove.md) | Remove um único objeto de [**certificado**](certificate.md) da coleção.<br/> (Herdado de **CertificatesICertificates2**)                            |
| [**Salvar**](certificates-save.md)     | Salva os certificados em um arquivo especificado.<br/> (Herdado de **CertificatesICertificates2**)                                                                |
| [**Não**](certificates-select.md) | Exibe uma caixa de diálogo para selecionar certificados e retorna uma coleção desses certificados selecionados.<br/> (Herdado de **CertificatesICertificates2**)  |



 

### <a name="properties"></a>Propriedades

O objeto **Certificates** tem essas propriedades.



| Propriedade                                             | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contagem**](certificates-count.md)<br/>       | Somente leitura<br/> | Recupera o número de objetos de [**certificado**](certificate.md) na coleção.<br/>                                                                                                                                |
| [**Item**](certificates-item.md)<br/>         | Somente leitura<br/> | Recupera um objeto de [**certificado**](certificate.md) que representa o certificado indexado da coleção. Essa é a propriedade padrão.<br/> (Herdado de **CertificatesICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Comentários

O objeto **Certificates** pode ser criado e é seguro para scripts. O ProgID do objeto de **certificados** é "CAPICOM. Certificados. 2 ".

**CAPICOM 1. *x*:** o ProgID para o objeto de **certificados** é "CAPICOM. Certificates. 1 ".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
