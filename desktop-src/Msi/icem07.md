---
description: ICEM07 verifica se a ordem dos arquivos na tabela de sequência corresponde à ordem dos arquivos no MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828713"
---
# <a name="icem07"></a>ICEM07

ICEM07 verifica se a ordem dos arquivos na tabela de sequência corresponde à ordem dos arquivos no [MergeModule.CABinet](mergemodule-cabinet.md).

O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.

## <a name="result"></a>Resultado

ICEM07 lançará um erro se a ordem dos arquivos na tabela de arquivos não corresponder à ordem no arquivo de gabinete.

## <a name="example"></a>Exemplo

IC0M07 publicaria a seguinte mensagem de erro para o exemplo mostrado.

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[File Table](file-table.md)



| Arquivo          | Sequência |
|---------------|----------|
| FileA. *GUID1* | 1        |
| FileB. *GUID1* | 8        |
| FileC. *GUID1* | 52       |



 

[MergeModule.CABda inet](mergemodule-cabinet.md) inserida



| Arquivo          |
|---------------|
| FileA. *GUID1* |
| FileC. *GUID1* |
| Arquiva. *GUID1* |
| FileB. *GUID1* |



 

Embora os números de sequência de arquivos na tabela de arquivos não precisem ser consecutivos e arquivos extras possam existir no arquivo de gabinete, a sequência relativa de todos os arquivos na tabela de arquivos deve corresponder à ordem no [MergeModule.CABinet](mergemodule-cabinet.md). Para corrigir esse erro, altere o número de sequência de FileB para que ele chegue após FileC para corresponder à ordem do arquivo no CAB ou reconstrua o CAB com os arquivos na ordem correta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



