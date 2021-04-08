---
title: Atributos únicos versus múltiplos valores
description: Os atributos que podem existir em um diretório são normalmente definidos no esquema para o diretório.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- ADSI de atributos de valor único vs. Multiple
- atributos ADSI, simples versus vários valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004855"
---
# <a name="single-vs-multiple-value-attributes"></a>Atributos únicos versus múltiplos valores

Os atributos que podem existir em um diretório são normalmente definidos no esquema para o diretório. A definição de esquema de um atributo especifica um número de características do atributo, como o tipo de dados e se uma instância do atributo pode ter vários valores.

Uma instância de um atributo de valor único pode conter um único valor. Uma instância de um atributo de múltiplos valores pode conter um único valor ou vários valores. Active Directory não cria atributos com valores vazios — ou o atributo contém um valor válido ou não existe no objeto.

> [!Note]  
> No Active Directory e a maioria dos outros servidores LDAP, a ordem dos valores em um atributo com valores múltiplos é indefinida. Além disso, cada valor de um atributo com valores múltiplos deve ser exclusivo.

 

A ADSI normalmente carrega dados de esquema se o diretório der suporte a um esquema, como Active Directory. Como a ADSI conhece a sintaxe dos atributos no esquema, não é necessário especificar o tipo de atributo ao acessá-lo. A ADSI realiza marshaling de valores de atributo para o tipo de dados apropriado, conforme definido no esquema.

Se o diretório não tiver nenhum esquema, forneça o tipo de dados ao acessar um atributo.

> [!Note]  
> Active Directory, Exchange, Windows NT 4,0 e servidor do site têm um esquema. Além disso, Active Directory tem um esquema extensível.

 

 

 




