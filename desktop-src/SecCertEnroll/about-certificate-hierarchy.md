---
description: Como o número de certificados emitidos em uma infraestrutura de chave pública (PKI) aumenta, pode se tornar difícil para uma única autoridade de certificação (CA) controlar efetivamente os certificados emitidos.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Hierarquia de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc3420e3f0f09f88b4b9e7157ec8abacc9516520de4472a48189520e3e0e567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904966"
---
# <a name="certificate-hierarchy"></a>Hierarquia de certificados

Como o número de certificados emitidos em uma infraestrutura de chave pública (PKI) aumenta, pode se tornar difícil para uma única autoridade de certificação (CA) controlar efetivamente os certificados emitidos. Uma maneira de resolver isso é criar uma hierarquia de certificados na qual a autoridade de certificação delega a autoridade para emitir certificados para autoridades subordinadas que podem, por sua vez, delegar autoridade a suas subordinadas. Cada autoridade de certificação Delega autoridade emitindo um certificado de autoridade de certificação para um subordinado. A autoridade de certificação inicial na cadeia é chamada de raiz, e não é necessário que uma entidade estabeleça confiança com qualquer AC que resida em uma [cadeia de certificados](about-certificate-chain.md) diferente da qual a entidade reside.

A ilustração a seguir mostra uma hierarquia de certificado composta de uma CA raiz, duas CAs subordinadas à raiz (uma para o departamento de marketing e outra para o departamento de produção) e CAs subordinadas a elas.

![diagrama de hierarquia de certificado](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de confiança](about-trust-models.md)
</dt> </dl>

 

 



