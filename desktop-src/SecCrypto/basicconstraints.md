---
description: Representa a extensão de restrições básicas de um certificado.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Objeto BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8cda73c4a698d40a602b39fd7822dabfbded9a7a35c27db16ca74f7993f7f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879516"
---
# <a name="basicconstraints-object"></a>Objeto BasicConstraints

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, [**use a Classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

O **objeto BasicConstraints** representa a extensão de restrições básicas de um certificado.

## <a name="when-to-use"></a>Quando usar

O **objeto BasicConstraints** é usado para executar as seguintes tarefas:

-   Determine se a extensão de restrições básicas está presente.
-   Determine se a extensão de restrições básicas está marcada como crítica.
-   Determine se o certificado é restrito a autoridades de certificação.
-   Determine se a restrição de comprimento do caminho está presente e recupere o valor da restrição de comprimento do caminho.

## <a name="members"></a>Membros

O **objeto BasicConstraints** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto BasicConstraints** tem essas propriedades.



| Propriedade                                                                                     | Tipo de acesso          | Descrição                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCertificateAuthority**](basicconstraints-iscertificateauthority.md)<br/>         | Somente leitura<br/> | Recupera um valor booliana que indica se o certificado é para uma AC (autoridade [*de certificação).*](../secgloss/c-gly.md)<br/> |
| [**Iscritical**](basicconstraints-iscritical.md)<br/>                                 | Somente leitura<br/> | Recupera um valor booliana que indica se a extensão de restrição básica está marcada como crítica.<br/>                                                                                                     |
| [**IsPathLenConstraintPresent**](basicconstraints-ispathlenconstraintpresent.md)<br/> | Somente leitura<br/> | Recupera um valor booliana que indica se a restrição de comprimento do caminho do certificado está presente.<br/>                                                                                                   |
| [**IsPresent**](basicconstraints-ispresent.md)<br/>                                   | Somente leitura<br/> | Recupera um valor booliana que indica se a extensão de restrições básicas está presente. Essa é a propriedade padrão.<br/>                                                                              |
| [**PathLenConstraint**](basicconstraints-pathlenconstraint.md)<br/>                   | Somente leitura<br/> | Recupera o valor da restrição de comprimento do caminho.<br/>                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

O **objeto BasicConstraints** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> </dl>

 

 
