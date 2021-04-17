---
description: A seção de instalação de um arquivo INF define as etapas do procedimento de instalação.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Exemplo de seção de instalação INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754939"
---
# <a name="inf-install-section-example"></a>Exemplo de seção de instalação INF

A seção de **instalação** de um arquivo inf define as etapas do procedimento de instalação. Cada linha de uma seção de **instalação** tem duas partes. À esquerda do sinal de igual (=) está a chave. No lado direito, é uma lista de um ou mais títulos de seção. A chave especifica o tipo das seções listadas à direita. Para obter uma descrição do formato desta seção, consulte "seções e diretivas de arquivo INF" do Microsoft Windows 2000 Driver Development Kit.

Veja a seguir um exemplo de uma seção de **instalação** .

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

Neste exemplo, a chave **CopyFiles** é definida com os valores "DataFiles" e "ProgramFiles". Isso especifica duas seções de **arquivos de cópia** no arquivo inf que contêm os nomes dos arquivos de origem usados por operações de cópia. O destino dos arquivos copiados seria especificado em uma seção **DestinationDirs** no arquivo inf.

A chave **DelFiles** recebe o valor "OldFiles". Isso especifica uma seção **Excluir arquivos** que contém informações relevantes para operações de exclusão de arquivos.

A chave **UpdateInis** especifica as seções do **arquivo ini de atualização** que contêm informações sobre a atualização de entradas no arquivo ini.

As chaves **AddReg** e **DelReg** especificam as seções **adicionar registro** e **Excluir registro** que contêm informações sobre como adicionar ou excluir informações do registro.

 

 



