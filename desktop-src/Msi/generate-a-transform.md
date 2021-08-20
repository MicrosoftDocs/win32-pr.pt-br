---
description: O arquivo VBScript WiGenXfm.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores. Este script de exemplo pode gerar uma transformação de dois bancos de Windows do Instalador. Para obter mais informações, consulte Transforms de banco de dados.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Gerar uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba16c894ec32bf300f1572eb26311be70315872b9711ca46573ce65e18802308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142763"
---
# <a name="generate-a-transform"></a>Gerar uma transformação

O arquivo VBScript WiGenXfm.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) Este script de exemplo pode gerar uma transformação de dois bancos de Windows do Instalador. Para obter mais informações, consulte [Transformações de banco de dados](database-transforms.md).

O exemplo demonstra o uso de:

[**Método OpenDatabase (Objeto do Instalador)**](installer-opendatabase.md)

[**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto Installer**](installer-object.md)

[**Método GenerateTransform do**](database-generatetransform.md) objeto [ **Database**](database-object.md)

Você exigirá a versão CScript.exe ou WScript.exe do host Windows Script para usar este exemplo. Para usar CScript.exe executar este exemplo, digite uma linha de comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiGenXfm.vbs \[ caminho do banco de dados original para o caminho revisado do banco de dados para \] \[ transformar o \] \[ arquivo\]**

Especifique o caminho para o banco de dados Windows Instalador original. Especifique o caminho para o banco de dados revisado. Especifique o caminho para o arquivo de transformação a ser criado. Se o caminho para o arquivo de transformação for omitido, os dois bancos de dados serão comparados apenas.

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows Host de Script, consulte Windows Ferramentas de Desenvolvimento [do Instalador](windows-installer-development-tools.md)do .

Observe que [um exemplo de localização](a-localization-example.md) demonstra [a geração de uma transformação de personalização.](generating-a-customization-transform.md)

 

 



