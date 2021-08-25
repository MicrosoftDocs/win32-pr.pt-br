---
description: É semelhante a uma opção de linha de comando. No entanto, você não precisa reinserar um comando \# pragma sempre que compilar um arquivo MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3cb9541ceef51119ce521244282920ca88397afe13290e99bdc14ce7d98ab55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860556"
---
# <a name="pragma"></a>\#Pragma

O **\# comando de pré-processador pragma** é semelhante a uma opção de linha de comando. No entanto, você não precisa reinserar um comando **\# pragma** sempre que compilar um arquivo MOF. O exemplo a seguir ilustra a **\# sintaxe de comando pragma:**


```mof
#pragma [command]
```



Normalmente, você coloca **\# um comando pragma** no início de um arquivo MOF. No entanto, você pode colocar alguns comandos, como o **\# comando pragma,** no corpo do código MOF. O exemplo a seguir mostra comandos **\# pragma** que indicam ao compilador MOF que ele deve colocar classes e instâncias no \\ namespace raiz cimv2 e compilar o arquivo no qual os comandos são incluídos durante a recuperação do repositório:


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



O exemplo a seguir lista os comandos **\# pragma** disponíveis.



| Comando                                         | Descrição                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Alteração**](pragma-amendment.md)           | Direciona o compilador MOF para separar um arquivo MOF em versões específicas do idioma e neutras ao idioma. |
| [**Autorecuperação**](pragma-autorecover.md)       | Adiciona um arquivo MOF à lista de arquivos compilados durante a recuperação do repositório.                             |
| [**classflags**](pragma-classflags.md)         | Controla a maneira como as classes são criadas ou atualizadas dependendo dos sinalizadores especificados.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Exclui uma classe existente e suas instâncias do repositório.                                      |
| [**deleteinstance**](pragma-deleteinstance.md) | Exclui uma instância existente de uma classe do repositório.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Controla a maneira como as instâncias são criadas ou atualizadas dependendo dos sinalizadores especificados.                   |
| [**Namespace**](pragma-namespace.md)           | Solicita que o compilador carregue o arquivo MOF no namespace especificado como *namespacepath*.         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 



