---
description: Algoritmos com suporte no Microsoft Base DSS e no provedor de criptografia Diffie-Hellman.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Algoritmos de provedor de PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748865"
---
# <a name="prov_dss_dh-provider-algorithms"></a>\_Algoritmos de provedor do Prov DSS \_ DH

A tabela a seguir lista os algoritmos suportados pelo Microsoft Base DSS e Diffie-Hellman provedor criptográfico.



| ID do algoritmo      | Descrição                                 | Comentários                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ MD5         | Algoritmo de hash MD5.                      | Fornecido somente para hash.                                                                                      |
| CALG \_ Sha         | Algoritmo de hash SHA.                      | Deve ser usado para assinaturas DSS.                                                                                |
| CALG \_ SHA1        | O mesmo que CALG \_ Sha.                          | Sem comentários.                                                                                                     |
| \_sinal DSS \_ CALG   | Algoritmo de assinatura de chave pública/privada DSS. | Comprimento da chave: pode ser definido, 512 bits a 1.024 bits em incrementos de bits 64. Comprimento de chave padrão: 1.024 bits.<br/> |
| CALG \_ DH \_ it      | Armazene e encaminhe a troca de chaves D-H.         | Comprimento da chave: pode ser definido, 384 bits a 512 bits em incrementos de 8 bits. Comprimento de chave padrão: 512 bits.<br/>      |
| CALG \_ DH \_ EPHEM   | Troca de chaves efêmeras D-H.                 | Comprimento da chave: pode ser definido, 384 bits a 512 bits em incrementos de 8 bits. Comprimento de chave padrão: 512 bits.<br/>      |
| CALG \_ CYLINK \_ MEK | Uma variante de 40 bits de uma chave DES.              | Comprimento da chave: 40 bits.                                                                                            |



 

 

 




