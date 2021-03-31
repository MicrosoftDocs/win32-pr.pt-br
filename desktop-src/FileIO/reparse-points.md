---
description: Descreve pontos de nova análise.
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: Pontos de reanálise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ad17af8993da500154dd88690420a563886f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829570"
---
# <a name="reparse-points"></a>Pontos de reanálise

Um arquivo ou diretório pode conter um *ponto de nova análise*, que é uma coleção de dados definidos pelo usuário. O formato desses dados é compreendido pelo aplicativo que armazena os dados e um filtro do sistema de arquivos, que você instala para interpretar os dados e processar o arquivo. Quando um aplicativo define um ponto de nova análise, ele armazena esses dados, além de uma *marca de nova análise*, que identifica exclusivamente os dados que estão sendo armazenados. Quando o sistema de arquivos abre um arquivo com um ponto de nova análise, ele tenta localizar o filtro do sistema de arquivos associado ao formato de dados identificado pela marca de nova análise. Se um filtro do sistema de arquivos for encontrado, o filtro processará o arquivo conforme direcionado pelos dados de nova análise. Se um filtro do sistema de arquivos não for encontrado, a operação de abertura de arquivo falhará.

Por exemplo, os pontos de nova análise são usados para implementar links do sistema de arquivos NTFS e o Microsoft Remote Storage Server (RSS). O RSS usa um conjunto de regras definido pelo administrador para mover arquivos usados raramente para o armazenamento de longo prazo, como fita ou mídia óptica. Ele usa pontos de nova análise para armazenar informações sobre o arquivo no sistema de arquivos. Essas informações são armazenadas em um arquivo stub que contém um ponto de nova análise cujos dados apontam para o dispositivo onde o arquivo real agora está localizado. O filtro do sistema de arquivos pode usar essas informações para recuperar o arquivo.

Os pontos de nova análise também são usados para implementar pastas montadas. Para obter mais informações, consulte [determinando se um diretório é uma pasta montada](determining-whether-a-directory-is-a-volume-mount-point.md).

As seguintes restrições se aplicam a pontos de nova análise:

-   Pontos de nova análise podem ser estabelecidos para um diretório, mas o diretório deve estar vazio. Caso contrário, o sistema de arquivos NTFS falhará ao estabelecer o ponto de nova análise. Além disso, você não pode criar diretórios ou arquivos em um diretório que contenha um ponto de nova análise.
-   Os pontos de nova análise e os atributos estendidos são mutuamente exclusivos. O sistema de arquivos NTFS não pode criar um ponto de nova análise quando o arquivo contém atributos estendidos e não pode criar atributos estendidos em um arquivo que contenha um ponto de nova análise.
-   Os dados do ponto de nova análise, incluindo a marca e o **GUID** opcional, não podem exceder 16 quilobytes. A definição de um ponto de nova análise falhará se a quantidade de dados a serem colocados no ponto de nova análise exceder esse limite.
-   Há um limite de 63 pontos de nova análise em qualquer caminho especificado.

    **Windows Server 2003 e Windows XP:** Há um limite de 31 pontos de nova análise em qualquer caminho especificado.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Marcas de ponto de nova análise](reparse-point-tags.md)<br/>                                 | Cada ponto de nova análise tem uma marca de identificador para que você possa diferenciar com eficiência os diferentes tipos de pontos de nova análise, sem precisar examinar os dados definidos pelo usuário no ponto de nova análise.<br/> |
| [Operações de ponto de nova análise](reparse-point-operations.md)<br/>                     | Descreve as operações de ponto de nova análise que você pode executar usando [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol).<br/>                                                                                       |
| [Pontos de nova análise e operações de arquivo](reparse-points-and-file-operations.md)<br/> | Descreve como os pontos de nova análise permitem o comportamento do sistema de arquivos que faz parte do comportamento que a maioria dos desenvolvedores do Windows espera.<br/>                                                                                     |



 

 

