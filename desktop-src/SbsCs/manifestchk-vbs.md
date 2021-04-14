---
description: O arquivo VBScript Manifestchk.vbs é uma ferramenta de validação fornecida no SDK (Software Development Kit) do Microsoft Windows que valida os arquivos de manifesto do aplicativo e do assembly.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370688"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

O arquivo VBScript Manifestchk.vbs é uma ferramenta de validação fornecida no SDK (Software Development Kit) do Microsoft Windows que valida os arquivos de manifesto do aplicativo e do assembly.

A execução deste exemplo requer o Windows Script Host. Para obter mais informações sobre o Windows Script Host, consulte a seção Windows Script Host do SDK do Windows. O Windows Script Host é, na verdade, dois hosts. CScript.exe é a versão que permite executar scripts no prompt de comando. CScript.exe fornece opções de linha de comando para definir propriedades de script.

O formato de linha de comando é o seguinte:

**Cscript//nologo manifestchk.vbs/s:** *\[ unidade: \] \[ caminho \] schemafilename* **/m:** *\[ unidade: \] \[ caminho \] ManifestFileName* **\[ /q \] /t:** *Option*

Os sinalizadores definidos para Manifestchk.vbs são descritos na tabela a seguir.



| Sinalizador | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | Especifica o nome do arquivo do esquema de manifesto no qual validar os manifestos. Consulte o esquema no [esquema do arquivo de manifesto](manifest-file-schema.md).                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | Especifica o nome do arquivo de manifesto a ser validado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | Suprime toda a saída para o console.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | Especifica o tipo de arquivo de manifesto. Os valores válidos são: é validar o [esquema do arquivo de manifesto](manifest-file-schema.md) de um [manifesto do assembly](assembly-manifests.md) ou do [manifesto do aplicativo](application-manifests.md)<br/> PC valida o [esquema do arquivo de configuração do Publicador](publisher-configuration-file-schema.md) de um [arquivo de configuração do Publicador](publisher-configuration-files.md)<br/> AC valide o esquema do arquivo de configuração de aplicativo de um [arquivo de configuração de aplicativo](application-configuration-files.md).<br/> |



 

Se o sinalizador/q não for especificado, Manifestchk.vbs exibirá informações detalhadas sobre o primeiro erro encontrado no arquivo e exibirá uma mensagem informando se o processo de validação foi bem-sucedido ou não.

Este utilitário verifica o seguinte:

-   Uma linha de comando válida.
-   A versão 3 do MSXML está instalada.
-   Se o manifesto usa XML bem formado.
-   O manifesto concorda com o esquema fornecido. Observe que Manifestchk.vbs verifica o arquivo de manifesto com base apenas no que é especificado no esquema fornecido. Para obter um exemplo de um esquema de manifesto, consulte o [esquema do arquivo de manifesto](manifest-file-schema.md).

Cscript.exe retornará um valor de 0 se o processo de validação tiver sido bem-sucedido e 1 se não tiver sido bem-sucedido. Ele retornará 2 se houver um erro em um argumento de linha de comando.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento lado a lado do assembly](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




