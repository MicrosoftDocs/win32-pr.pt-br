---
description: O arquivo VBScript WiGenXfm.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este script de exemplo pode gerar uma transformação de dois bancos de dados Windows Installer. Para obter mais informações, consulte transformações de banco de dados.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Gerar uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662536"
---
# <a name="generate-a-transform"></a>Gerar uma transformação

O arquivo VBScript WiGenXfm.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este script de exemplo pode gerar uma transformação de dois bancos de dados Windows Installer. Para obter mais informações, consulte [transformações de banco de dados](database-transforms.md).

O exemplo demonstra o uso de:

[**Método OpenDatabase (objeto instalador)**](installer-opendatabase.md)

[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)

[**Método GenerateTransform**](database-generatetransform.md) do [ **objeto Database**](database-object.md)

Você precisará da versão CScript.exe ou WScript.exe do Windows Script Host para usar este exemplo. Para usar CScript.exe para executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiGenXfm.vbs \[ caminho para o caminho do banco de dados original \] \[ para o caminho do banco de dados revisado \] \[ para transformar\]**

Especifique o caminho para o banco de dados de Windows Installer original. Especifique o caminho para o banco de dados revisado. Especifique o caminho para o arquivo de transformação a ser criado. Se o caminho para o arquivo de transformação for omitido, os dois bancos de dados serão comparados apenas.

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

Observe que [um exemplo de localização](a-localization-example.md) demonstra [a geração de uma transformação de personalização](generating-a-customization-transform.md).

 

 



