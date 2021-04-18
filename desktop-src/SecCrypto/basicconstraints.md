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
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766831"
---
# <a name="basicconstraints-object"></a>Objeto BasicConstraints

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

O objeto **BasicConstraints** representa a extensão de restrições básicas de um certificado.

## <a name="when-to-use"></a>Quando usar

O objeto **BasicConstraints** é usado para executar as seguintes tarefas:

-   Determine se a extensão de restrições básicas está presente.
-   Determine se a extensão de restrições básicas está marcada como crítica.
-   Determine se o certificado está restrito às autoridades de certificação.
-   Determine se a restrição de comprimento do caminho está presente e recupere o valor da restrição de comprimento do caminho.

## <a name="members"></a>Membros

O objeto **BasicConstraints** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **BasicConstraints** tem essas propriedades.



| Propriedade                                                                                     | Tipo de acesso          | Descrição                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCertificateAuthority**](basicconstraints-iscertificateauthority.md)<br/>         | Somente leitura<br/> | Recupera um valor booliano que indica se o certificado é para uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA).<br/> |
| [**IsCritical**](basicconstraints-iscritical.md)<br/>                                 | Somente leitura<br/> | Recupera um valor booliano que indica se a extensão de restrição básica está marcada como crítica.<br/>                                                                                                     |
| [**IsPathLenConstraintPresent**](basicconstraints-ispathlenconstraintpresent.md)<br/> | Somente leitura<br/> | Recupera um valor booliano que indica se a restrição de comprimento de caminho do certificado está presente.<br/>                                                                                                   |
| [**IsPresent**](basicconstraints-ispresent.md)<br/>                                   | Somente leitura<br/> | Recupera um valor booliano que indica se a extensão de restrições básica está presente. Essa é a propriedade padrão.<br/>                                                                              |
| [**PathLenConstraint**](basicconstraints-pathlenconstraint.md)<br/>                   | Somente leitura<br/> | Recupera o valor da restrição de comprimento do caminho.<br/>                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

O objeto **BasicConstraints** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> </dl>

 

 
