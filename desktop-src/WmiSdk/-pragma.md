---
description: É semelhante a uma opção de linha de comando. No entanto, você não precisa inserir novamente um \# comando pragma sempre que compilar um arquivo MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813441"
---
# <a name="pragma"></a>\#pragma

O comando de pré-processador de **\# pragma** é semelhante a uma opção de linha de comando. No entanto, você não precisa inserir novamente um comando **\# pragma** sempre que COMPILAR um arquivo MOF. O exemplo a seguir ilustra a sintaxe do comando **\# pragma** :


```mof
#pragma [command]
```



Normalmente, você coloca um comando **\# pragma** no início de um arquivo MOF. No entanto, você pode inserir alguns comandos, como o comando **\# pragma** , no corpo do código MOF. O exemplo a seguir mostra os comandos **\# pragma** que indicam ao compilador MOF que ele deve posicionar classes e instâncias no \\ namespace raiz cimv2 e compilar o arquivo no qual os comandos são incluídos durante a recuperação do repositório:


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



O seguinte lista os comandos de **\# pragma** disponíveis.



| Comando                                         | Descrição                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**aditamento**](pragma-amendment.md)           | Direciona o compilador MOF para separar um arquivo MOF em versões de idioma neutros e específicas de idiomas. |
| [**AutoRecuperação**](pragma-autorecover.md)       | Adiciona um arquivo MOF à lista de arquivos compilados durante a recuperação do repositório.                             |
| [**classflags**](pragma-classflags.md)         | Controla a maneira como as classes são criadas ou atualizadas dependendo dos sinalizadores especificados.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Exclui uma classe existente e suas instâncias do repositório.                                      |
| [**deleteinstance**](pragma-deleteinstance.md) | Exclui uma instância existente de uma classe do repositório.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Controla a maneira como as instâncias são criadas ou atualizadas dependendo dos sinalizadores especificados.                   |
| [**namespace**](pragma-namespace.md)           | Solicita que o compilador carregue o arquivo MOF no namespace especificado como *NamespacePath*.         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 



