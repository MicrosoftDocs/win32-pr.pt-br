---
description: Pesquisando arquivos de assembly
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: Pesquisando arquivos de assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7be73b162ea41fd9eeb0a042a1fc2e202b8115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171279"
---
# <a name="searching-for-assembly-files"></a>Pesquisando arquivos de assembly

Contextos de ativação podem ajudar o carregador a localizar arquivos de assembly. Quando o carregador procura um arquivo para carregar por nome, ele primeiro procura por arquivos com o nome especificado que são referenciados por assemblies que são membros do contexto de ativação ativo no momento. Uma chamada para [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) também localiza esses arquivos primeiro. Os arquivos que têm o nome especificado e o contexto de ativação atual são encontrados e carregados antes dos arquivos com o nome no diretório local ou na variável de ambiente PATH. Isso significa que, ao criar manifestos, você precisa listar todos os arquivos que planeja usar com as importações **SearchPath**, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)ou estáticas.

Observe que esses arquivos não são localizados automaticamente ao usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou outras funções que não pesquisam arquivos. Para usar esses arquivos com **CreateFile**, use [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) primeiro para localizar o caminho para o arquivo isolado e, em seguida, use **CreateFile** no caminho retornado.

Esse método de pesquisa de arquivos ajuda a manter os aplicativos isolados separados porque vários arquivos com o mesmo nome podem, então, diferir somente por sua associação com assemblies de números de versão diferentes. O sistema operacional pode encontrar o arquivo correto a ser usado durante operações de arquivo.

Se uma DLL for carregada dessa maneira usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya), o DllMain (ponto de entrada) da dll será chamado enquanto o contexto de ativação original for mantido ativo, exceto se a própria DLL contiver um manifesto em uma determinada ID de recurso ( \_ ID de \_ recurso de manifesto ISOLATIONAWARE \_ ou 2)

 

 
