---
description: O método recomendado para gerar um pacote de patch é usar ferramentas de criação de patch, como Msimsp.exe e Patchwiz.dll. A Msimsp.exe do Msimsp.exe está disponível apenas nos componentes do SDK Windows para desenvolvedores Windows Instalador.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa82f2fbefc9046877f4f98cf4a3c126d94e6542b60076f0491bd0f311ee00a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627792"
---
# <a name="msimspexe"></a>Msimsp.exe

O método recomendado para gerar um pacote de patch é usar ferramentas de criação de patch, como Msimsp.exe e [Patchwiz.dll](patchwiz-dll.md). A Msimsp.exe do Msimsp.exe está disponível apenas nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md)

Msimsp.exe é um arquivo executável que chama [Patchwiz.dll](patchwiz-dll.md). A ferramenta pode ser usada para criar um pacote de patch passando o caminho para um arquivo de propriedades de criação de patch (arquivo .pcp) e o caminho para o pacote de patch que está sendo criado. Msimsp.ex também pode ser usado para criar um arquivo de log e especificar uma pasta temporária na qual as transformaçãos, os gabinetes e os arquivos usados para criar o pacote de patch são salvos.

A sintaxe de linha de comando para Msimsp.exe é:

**Msimsp.exe -s** *\[ para o arquivo \] .pcp* **-p** *\[ caminho \] para o arquivo .msp* **{options}**

As opções de linha de comando não são sensíveis a minúsculas e delimitadores de barra podem ser usados em vez de um traço. Se nenhuma opção for especificada, Msimsp.exe exibirá os valores atuais das propriedades de informações resumidas.

<dl> <dt>

<span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ caminho para o \] arquivo .pcp_
</dt> <dd>

Isso é necessário e deve ser seguido pelo caminho para o arquivo de propriedades de criação de patch (extensão .pcp). Para obter mais informações, [ consultePatchWiz.dll](patchwiz-dll.md).

</dd> <dt>

<span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**Caminho -p**_para o arquivo .msp_
</dt> <dd>

Isso é necessário e seguido pelo caminho para o pacote de patch que está sendo criado (extensão .msp).

</dd> <dt>

<span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_caminho para a pasta temporária_
</dt> <dd>

Opcional. Seguido pelo caminho para a pasta temporária. O local padrão é %TMP% \\ ~pcw \_ tmp.tmp \\ .

</dd> <dt>

<span id="-k"></span><span id="-K"></span>**-k**
</dt> <dd>

Opcional. Falhará se a pasta temporária já existir.

</dd> <dt>

<span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l caminho**_para o arquivo de log_
</dt> <dd>

Opcional. Seguido pelo caminho para o arquivo de log que descreve o processo de criação de patch e erros. Para obter mais informações, [consulte Valores de retorno para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

</dd> <dt>

<span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_caminho para o arquivo de log com dados de desempenho_
</dt> <dd>

Opcional. Seguido pelo caminho para o arquivo de log que descreve o processo de criação de patch e erros. Essa opção grava dados de desempenho no arquivo de log. Essa opção requer a versão 4.0 do Patchwiz.dll.

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
> Msimsp.exe poderá falhar quando chamar Makecab.exe se houver valores na coluna Arquivo [](file-table.md) da tabela Arquivo do pacote de instalação que diferem apenas por caso. Windows O instalador diferencia minúsculas e permite um pacote de instalação, como na tabela abaixo, somente quando Comp1 e Comp2 são instalados em diretórios diferentes. No entanto, nesse cenário, você não pode usar Msimsp.exe [ ouPatchwiz.dll](patchwiz-dll.md) para gerar um patch para o pacote, porque Msimsp.exe e Patchwiz.dll chamada Makecab.exe, o que não faz sentido para maiúsculas e minúsculas.
> 
> Evite a adoção de um pacote de instalação, como a tabela [De arquivos parcial a seguir.](file-table.md)
> 
> | Arquivo       | Componente\_ | FileName   |
> |------------|-------------|------------|
> | readme.txt | Comp1       | readme.txt |
> | ReadMe.txt | Comp2       | readme.txt |


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um pacote de patch](creating-a-patch-package.md)
</dt> <dt>

[Um pequeno exemplo de a patch de atualização](a-small-update-patching-example.md)
</dt> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis lançados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



