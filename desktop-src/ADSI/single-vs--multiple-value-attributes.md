---
title: Atributos de valor único vs. múltiplo
description: Os atributos que podem existir em um diretório normalmente são definidos no esquema do diretório.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- ADSI de atributos de valor único vs. vários valores
- atributos ADSI , atributos de valor único versus vários valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd9442a5365efbe343c2a9af74aa8576928e7a6a383cc131a3384152c2b1c0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262026"
---
# <a name="single-vs-multiple-value-attributes"></a>Atributos de valor único vs. múltiplo

Os atributos que podem existir em um diretório normalmente são definidos no esquema do diretório. A definição de esquema de um atributo especifica várias características do atributo, como o tipo de dados e se uma instância do atributo pode ter vários valores.

Uma instância de um atributo de valor único pode conter um único valor. Uma instância de um atributo com vários valores pode conter um único valor ou vários valores. O Active Directory não cria atributos com valores vazios — o atributo contém um valor válido ou não existe no objeto .

> [!Note]  
> No Active Directory e na maioria dos outros servidores LDAP, a ordem dos valores em um atributo com vários valores é indefinida. Além disso, cada valor de um atributo com vários valores deve ser exclusivo.

 

O ADSI normalmente carregará dados de esquema se o diretório for compatível com um esquema, como o Active Directory. Como a ADSI conhece a sintaxe dos atributos no esquema, não é necessário especificar o tipo de atributo ao acessá-lo. ADSI marshals de valores de atributo para o tipo de dados apropriado, conforme definido no esquema.

Se o diretório não tiver esquema, fornece o tipo de dados ao acessar um atributo.

> [!Note]  
> O Active Directory, Exchange, Windows NT 4.0 e o Servidor do Site têm um esquema. Além disso, o Active Directory tem um esquema extensível.

 

 

 




