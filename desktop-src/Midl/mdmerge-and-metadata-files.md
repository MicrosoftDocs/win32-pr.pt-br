---
title: MDMERGE e arquivos de metadados
description: Compõe vários arquivos de metadados (. winmd) em um número de arquivos de metadados de saída, com base no namespace.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- arquivo winmd
- Metadados do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916005"
---
# <a name="mdmerge-and-metadata-files"></a>MDMERGE e arquivos de metadados

Compõe vários arquivos de metadados (. winmd) em um número de arquivos de metadados de saída, com base no namespace.

## <a name="usage"></a>Uso

Execute MDMERGE na linha de comando usando o seguinte comando:

 *< ***Opções*** de mdmerge>*

em que *< ***Opções*** >* representa as opções de linha de comando que você deseja usar.

Gere arquivos de metadados para seus componentes de Windows Runtime personalizados usando o compilador MIDLRT. Para obter mais informações, consulte [MIDLRT and Windows Runtime Components](midlrt-and-windows-runtime-components.md).

## <a name="command-line-switches"></a>Opções de linha de comando

A lista a seguir mostra as opções de linha de comando que o MDMERGE usa.

<dl>

[**/i**](-mdmerge-i.md)  
[**/Metadata \_ dir**](-mdmerge-metadata-dir.md)  
[**opção**](-mdmerge-n.md)  
[**/o**](-mdmerge-o.md)  
[**/partial**](-mdmerge-partial.md)  
[**/v**](-mdmerge-v.md)  
</dl>

Uma lista completa dos comutadores e opções do compilador MDMERGE está disponível quando você usa **-h** e **/?** comutadores.

## <a name="remarks"></a>Comentários

A composição de metadados permite que vários arquivos IDL contenham definições para Windows Runtime componentes no mesmo namespace. Isso libera você da definição de todos os tipos em um namespace dentro de um único arquivo IDL.

É provável que você tenha vários componentes Windows Runtime que seus aplicativos usam. Ao executar a etapa final para produzir assemblies de metadados implantáveis Windows Runtime, você pode configurar o MDMERGE para mesclar componentes de vários diretórios de metadados, como aqueles que são instalados com o sistema (% WINDOWS% \\ System32 \\ WinMetadata), seus tipos de base e o diretório de Build do projeto atual. Todos os tipos necessários são mesclados nos assemblies de metadados corretos, implantáveis, que você pode empacotar para a Windows Store.

Você pode usar a opção [**/n**](-mdmerge-n.md) para especificar a profundidade de namespace com suporte para compor assemblies de metadados. Isso permite configurar uma divisão a quente para seus componentes de Windows Runtime, de modo que apenas um único arquivo. winmd seja empacotado em vez de muitos. Isso reduz os tempos de carregamento e a e/s de arquivo exigidos por seus aplicativos da Windows Store.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes MIDLRT e Windows Runtime](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




