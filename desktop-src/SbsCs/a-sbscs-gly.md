---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (aplicativos isolados e assemblies lado a lado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780183"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a>A (aplicativos isolados e assemblies lado a lado)

A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contexto de ativação**
</dt> <dd>

Uma estrutura de dados na memória. Cada seção dessa estrutura contém metadados para funções de API com reconhecimento lado a lado. Por exemplo, uma seção pode ter dados de redirecionamento de DLL, que são usados pelo carregador de DLL e outro pode ter dados de servidor COM. Esses dados podem ser usados para redirecionar o carregamento de uma DLL para uma versão específica, a criação de um objeto COM ou a criação de uma janela para uma versão mais compatível para o aplicativo.

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configuração do aplicativo**
</dt> <dd>

Nomes e versões de assemblies lado a lado necessários para executar um aplicativo. Quando um aplicativo é implantado com um manifesto, as dependências em versões específicas de assemblies compartilhados lado a lado são explicitamente definidas. Por padrão, a versão do assembly especificado no manifesto é a versão que é usada na ativação. Configuração de aplicativo global especifica a configuração de todos os aplicativos no sistema. A configuração por aplicativo pode substituir a configuração de aplicativo global em uma base por aplicativo.

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifesto de configuração do aplicativo**
</dt> <dd>

Arquivo que especifica assemblies lado a lado a serem usados por um aplicativo totalmente ou parcialmente isolado. Os arquivos de manifesto de configuração do aplicativo são instalados na mesma pasta que o arquivo executável do aplicativo.

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifesto do aplicativo**
</dt> <dd>

Arquivo que descreve um aplicativo isolado. Ele especifica as informações necessárias para executar o aplicativo, incluindo dependências em assemblies privados, versões específicas de assemblies compartilhados e metadados para assemblies privados. O nome de um arquivo de manifesto do aplicativo é o nome do executável do aplicativo seguido pela extensão. manifest. Por exemplo, para MySampleApp.exe, o arquivo de manifesto seria MySampleApp.exe. manifest.

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**)**
</dt> <dd>

Unidade fundamental para nomeação, vinculação, controle de versão, implantação ou configuração de um bloco de código de programação. Esses assemblies de código podem ser colocados em DLLs ou assemblies COM. Aplicativos com funcionalidade comum podem executar blocos compartilhados de código de programação que são chamados de módulos ou assemblies de código. A infraestrutura para o compartilhamento seguro de assemblies é conhecida como compartilhamento de assembly lado a lado.

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifesto do assembly**
</dt> <dd>

Descrição de um assembly lado a lado. Ele especifica o nome, a versão, os arquivos, os recursos do assembly, os dados de associação para os itens do assembly e as dependências em outros assemblies lado a lado. Um arquivo de manifesto do assembly pode ter qualquer nome de arquivo válido, desde que seja seguido pela extensão. manifest.

</dd> </dl>

 

 



