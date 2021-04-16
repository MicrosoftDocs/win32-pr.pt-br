---
description: O método recomendado para gerar um pacote de patch é usar ferramentas de criação de patch, como Msimsp.exe e Patchwiz.dll. A ferramenta de Msimsp.exe só está disponível nos componentes SDK do Windows para desenvolvedores de Windows Installer.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105759212"
---
# <a name="msimspexe"></a>Msimsp.exe

O método recomendado para gerar um pacote de patch é usar ferramentas de criação de patch, como Msimsp.exe e [Patchwiz.dll](patchwiz-dll.md). A ferramenta de Msimsp.exe só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Msimsp.exe é um arquivo executável que chama [Patchwiz.dll](patchwiz-dll.md). A ferramenta pode ser usada para criar um pacote de patch passando o caminho para um arquivo de propriedades de criação de patch (arquivo. PCP) e o caminho para o pacote de patch que está sendo criado. Msimsp. ex também pode ser usado para criar um arquivo de log e especificar uma pasta temporária na qual as transformações, os gabinetes e os arquivos usados para criar o pacote de patch são salvos.

A sintaxe de linha de comando para Msimsp.exe é:

Caminho do **Msimsp.exe-s** *\[ para o arquivo \] . PCP* **-p** *\[ caminho para o \] arquivo. msp* **{Options}**

As opções de linha de comando não diferenciam maiúsculas de minúsculas e os delimitadores de barra podem ser usados em vez de um traço. Se nenhuma opção for especificada, Msimsp.exe exibirá os valores atuais das propriedades de informações de resumo.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ caminho para o arquivo \] . PCP_
</dt> <dd>

Isso é necessário e deve ser seguido pelo caminho para o arquivo de propriedades de criação de patch (extensão. PCP). Para obter mais informações, consulte [PatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_caminho para o arquivo. msp_
</dt> <dd>

Isso é necessário e seguido pelo caminho para o pacote de patches que está sendo criado (extensão. msp).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_caminho para a pasta temporária_
</dt> <dd>

Opcional. Seguido pelo caminho para a pasta temporária. O local padrão é% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

Opcional. Falha se a pasta temporária já existir.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_caminho para o arquivo de log_
</dt> <dd>

Opcional. Seguido pelo caminho para o arquivo de log que descreve o processo e os erros de criação de patch. Para obter mais informações, consulte [valores de retorno para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-caminho LP**_para arquivo de log com dados de desempenho_
</dt> <dd>

Opcional. Seguido pelo caminho para o arquivo de log que descreve o processo e os erros de criação de patch. Essa opção grava dados de desempenho no arquivo de log. Esta opção requer a versão 4,0 de Patchwiz.dll.

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Opcional. Exibe uma caixa de diálogo se a criação do patch for concluída com êxito.

</dd> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Exibe a ajuda de linha de comando.

</dd> </dl>

> [!Note]
> Msimsp.exe pode falhar ao chamar Makecab.exe se houver valores na coluna arquivo da [tabela de arquivos](file-table.md) do pacote de instalação que diferem apenas por maiúsculas e minúsculas. Windows Installer diferencia maiúsculas de minúsculas e permite um pacote de instalação, como na tabela a seguir, somente quando comp1 e Comp2 são instalados em diretórios diferentes. No entanto, nesse cenário, você não pode usar Msimsp.exe ou [Patchwiz.dll](patchwiz-dll.md) para gerar um patch para o pacote, pois Msimsp.exe e Patchwiz.dll chamada Makecab.exe, que não diferencia maiúsculas de minúsculas.
> 
> Evite criar um pacote de instalação, como a seguinte [tabela de arquivos](file-table.md)parcial.
> 
> | Arquivo       | Componente\_ | FileName   |
> |------------|-------------|------------|
> | readme.txt | Comp1       | readme.txt |
> | ReadMe.txt | Comp2       | readme.txt |


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um pacote de patch](creating-a-patch-package.md)
</dt> <dt>

[Um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md)
</dt> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



