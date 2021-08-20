---
description: a versão do PATCHWIZ.DLL lançada com Windows Installer&\# 160; 3.0 pode gerar automaticamente informações de sequenciamento de patch e adicionar à tabela MsiPatchSequence um novo patch.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Gerando informações de sequência de patch (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03094d9df26f4565db5b3a31c9a27c58a0bb45dac8aac93b2fefce34104d58c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947017"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a>Gerando informações de sequência de patch (PATCHWIZ.DLL)

a versão do [PATCHWIZ.DLL](patchwiz-dll.md) lançada com Windows Installer 3,0 pode gerar automaticamente informações de sequenciamento de patch e adicionar à [tabela MsiPatchSequence](msipatchsequence-table.md) um novo patch.

Defina a propriedade de geração de dados de sequência \_ \_ \_ desabilitada como 1 (uma) na [tabela Propriedades](properties-table-patchwiz-dll-.md) do arquivo. PCP para evitar a geração automática de informações de sequenciamento de patch. Se essa propriedade estiver ausente, as informações serão geradas e adicionadas automaticamente.

quando o [PATCHWIZ.DLL](patchwiz-dll.md) liberado com Windows Installer 3,0 é usado para gerar automaticamente as informações de sequenciamento de patch, ocorre o seguinte:

-   Uma nova linha é adicionada à [tabela MsiPatchSequence](msipatchsequence-table.md) para cada código de produto de uma imagem de destino listada na [tabela TargetImages](targetimages-table-patchwiz-dll-.md).
-   Os valores adicionados à coluna PatchFamily nas novas linhas correspondem aos códigos de produto de destino das imagens de destino listadas na [tabela TargetImages](targetimages-table-patchwiz-dll-.md).
-   Os valores adicionados às colunas de sequência nas novas linhas são gerados usando a versão de produto mais alta direcionada pelo patch e a hora UTC quando o patch é gerado. O número de sequência é <Product Minor Version> . <Build Major Number> . <carimbo de data/hora 1>. <carimbo de data/hora 2>.
    -   O primeiro campo é a versão do produto da versão mais recente do produto que é alvo do patch.
    -   O segundo campo é o número principal de compilação da versão mais recente do produto que é alvo do patch.

    Os dois campos de carimbo de data/hora contam com o carimbo de data/hora de 32 bits necessário para contar os segundos em UTC (tempo Universal Coordenado).
    > [!Note]  
    > As versões do produto têm o seguinte formato: <Product Major Version> . <Product Minor Version> . <Build Major Number> <Build Minor Number> e um produto com um número de versão 2.1.0.0 é uma versão superior à de um produto com o número de versão 1.2.0.0

     

-   O atributo msidbPatchSequenceSupersedeEarlier é inserido na coluna de atributo de novas linhas que são geradas para Service Packs (SP) ou patches de atualização secundária. O atributo msidbPatchSequenceSupersedeEarlier não é adicionado a um QFE ou um patch de atualização pequeno.
    > [!Note]  
    > Um service pack (SP) deve conter as correções de todos os QFEs que foram lançados antes dele. No entanto, se um autor de patch definir a propriedade de substituição de dados de sequência \_ \_ como 0 (zero) ou 1 (um) no arquivo. PCP, a coluna atributos de todas as linhas na tabela MsiPatchSequence será definida como o valor especificado para substituição de dados de sequência \_ \_ . Os autores de patches que exigem mais controle devem criar a coluna atributos manualmente.

     

Se você incluir uma [tabela PatchSequence](patchsequence-table--patchwiz-dll-.md) no arquivo. PCP, a propriedade de \_ geração de dados de sequência \_ \_ desabilitada será ignorada e as informações fornecidas na tabela PatchSequence poderão ser adicionadas à [tabela MsiPatchSequence](msipatchsequence-table.md) do patch.

 

 



