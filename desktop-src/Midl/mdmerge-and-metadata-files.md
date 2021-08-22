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
ms.openlocfilehash: 1a065a8ff93485728b1c5c4c0c7b43de88e3844a8a013f07caee8d85d76d721d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252426"
---
# <a name="mdmerge-and-metadata-files"></a>MDMERGE e arquivos de metadados

Compõe vários arquivos de metadados (. winmd) em um número de arquivos de metadados de saída, com base no namespace.

## <a name="usage"></a>Uso

Execute MDMERGE na linha de comando usando o seguinte comando:

**mdmerge**  *<* **Opções** do _>_

onde **as opções** * < * _>_ representam as opções de linha de comando que você deseja usar.

gere arquivos de metadados para seus componentes de Windows Runtime personalizados usando o compilador MIDLRT. para obter mais informações, consulte [MIDLRT and Windows Runtime components](midlrt-and-windows-runtime-components.md).

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

a composição de metadados permite que vários arquivos IDL contenham definições para Windows Runtime componentes no mesmo namespace. Isso libera você da definição de todos os tipos em um namespace dentro de um único arquivo IDL.

é provável que você tenha vários componentes Windows Runtime que seus aplicativos usam. ao executar a etapa final para produzir assemblies de metadados implantáveis Windows Runtime, você pode configurar o MDMERGE para mesclar componentes de vários diretórios de metadados, como aqueles que são instalados com o sistema (% Windows% \\ system32 \\ WinMetadata), seus tipos de base e o diretório de build do projeto atual. todos os tipos necessários são mesclados nos assemblies de metadados corretos, implantáveis, que você pode empacotar para o repositório de Windows.

Você pode usar a opção [**/n**](-mdmerge-n.md) para especificar a profundidade de namespace com suporte para compor assemblies de metadados. isso permite configurar uma divisão a quente para seus componentes de Windows Runtime, de modo que apenas um único arquivo. winmd seja empacotado em vez de muitos. isso reduz os tempos de carregamento e a e/s de arquivo exigidos por seus aplicativos da Windows Store.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[componentes MIDLRT e Windows Runtime](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




