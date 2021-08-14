---
description: Você pode importar e exportar chaves simétricas e chaves assimétricas com a CNG. E você pode usar a funcionalidade de exportação e importação de chave para mover chaves entre computadores.
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: Importação e exportação de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a4b6c26069911d771697bf06f7464aa14ab7f099e4a0e06991d2fd992efa44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907697"
---
# <a name="key-import-and-export"></a>Importação e exportação de chave

Você pode importar e exportar [*chaves simétricas*](/windows/desktop/SecGloss/s-gly) e chaves assimétricas com a CNG. E você pode usar a funcionalidade de exportação e importação de chave para mover chaves entre computadores.

## <a name="symmetric-keys"></a>Chaves simétricas

Para importar ou exportar chaves simétricas (ou de sessão) nas quais a mesma chave é usada para criptografar e descriptografar alguns dados, você pode usar as funções [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) e [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) . Normalmente, você primeiro exporta uma chave usando a função **BCryptExportKey** antes de importar usando a função **BCryptImportKey** . As funções são projetadas para habilitar a criptografia de chaves exportadas e importadas usando os parâmetros *hExportKey* e *hImportKey* ; no entanto, a implementação da Microsoft dessas funções não oferece suporte à criptografia de chaves exportadas e importadas.

## <a name="asymmetric-keys"></a>Chaves assimétricas

Para importar pares de chaves assimétricas (ou [*públicas/privadas*](/windows/desktop/SecGloss/p-gly)) em que uma chave é usada para criptografar e a outra é usada para descriptografar alguns dados, você pode usar qualquer uma das funções [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) ou [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) . Um provedor CNG deve codificar o par de chaves usando um tipo de [*blob de chave*](/windows/desktop/SecGloss/k-gly) com suporte. [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) pode ser usado para criar o blob de chave codificado. [estruturas CNG](cng-structures.md) descreve os principais tipos de BLOB e estruturas que o provedor de Armazenamento de chaves da Microsoft suporta.

Para [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) criar um par de chaves persistente, o blob de chave de entrada deve conter uma [*chave privada*](/windows/desktop/SecGloss/p-gly). [*As chaves públicas*](/windows/desktop/SecGloss/p-gly) não são persistentes.

O nome da chave e a política de exportação não fazem parte da estrutura de [*blob*](/windows/desktop/SecGloss/b-gly) definida em [estruturas CNG](cng-structures.md). No entanto, se um BLOB for de um tipo de BLOB opaco (como a imagem de memória de um estado de chave interna), o BLOB poderá conter as propriedades nome da chave e política de exportação.

O procedimento a seguir descreve como importar uma chave privada persistente com suas propriedades.

**Para importar uma chave persistente**

1.  Crie uma chave persistente usando a função [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) .
2.  Defina as propriedades desejadas no objeto de chave usando a função [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) .
3.  Defina o BLOB de importação de chave como uma propriedade na chave, com o tipo de BLOB como o nome da propriedade.
4.  Finalize a importação de chave persistente usando a função [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) .

 

 
