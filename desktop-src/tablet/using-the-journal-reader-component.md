---
description: O componente Leitor Windows Anotação de Diário da Microsoft fornece acesso de leitura programático a arquivos no formato Diário.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Usando o componente Leitor de Diário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41559ac31ff081ecb810b0fe6e82ce1107ed87dae897cc7e6b8be4569e9b78f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449175"
---
# <a name="using-the-journal-reader-component"></a>Usando o componente Leitor de Diário

O componente Leitor Windows Anotação de Diário da Microsoft fornece acesso de leitura programático a arquivos no formato Diário.

## <a name="component-overview"></a>Visão geral do componente

Os arquivos de diário têm a extensão de arquivo .jnt. Esse componente simples pega um fluxo que contém um arquivo .jnt e retorna um fluxo que contém o conteúdo do arquivo no formato XML. O XML retornado pelo componente está em conformidade com o esquema leitor de notas do diário. Esse esquema está documentado em Referência [de esquema de leitor de diário.](journal-reader-schema-reference.md)

O componente não fornece a capacidade de gravar arquivos .jnt.

O componente está disponível em versões gerenciadas e não gerenciadas. O componente nãomanaged está disponível na DLL (biblioteca journal.dll de vínculo dinâmico). A versão gerenciada está no assembly Microsoft.Ink.Journal.dll (para redistribuição para Windows XP Tablet PC Edition ou Windows Vista) ou Microsoft.Ink.dll.

> [!IMPORTANT]
>
> A partir Windows 10, versão 1607, o journal.dll não está incluído no Windows operacional. Essa biblioteca deve ser considerada preterida ou obsoleta e não deve ser usada.

 

### <a name="assembly-changes-of-note"></a>Alterações de nota do assembly

É importante estar ciente de algumas alterações no assembly que contém o componente Leitor de Notas do Diário que ocorreram entre a versão lançada em conjunto com a versão 1.7 do Tablet Developers Kit e a versão que é enviada no sistema operacional Windows Vista.

A versão 1.7 do componente de leitor, que pode ser redistribuída para o Windows XP ou Windows Vista, está contida em um assembly chamado Microsoft.Ink.Journal.dll. O componente leitor é Windows Vista, mas foi integrado ao assembly Microsoft.Ink.dll núcleo. Isso significa que os aplicativos que usam o assembly 1.7 precisam redistribuir esse assembly com sua configuração.

## <a name="using-the-component"></a>Usando o componente

O componente Leitor de Notas do Diário é útil para extrair os dados de tinta e outras informações sobre o arquivo de um arquivo de Diário.

### <a name="com"></a>COM

O componente COM do Leitor de Notas do Diário está no arquivo Journal.dll, que é instalado e registrado quando você baixa e executar o arquivo de instalação do Leitor de Notas do Diário.

O componente COM não dá suporte à interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

### <a name="managed"></a>Gerenciado

O componente gerenciado Leitor de Notas do Diário está no assembly Microsoft.Ink.JournalReader.dll diário. Esse assembly é instalado e registrado no cache de assembly global quando você executar o arquivo de instalação leitor de anotações do diário.

Adicione uma referência ao assembly para usá-la em seu projeto gerenciado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IJournalReader Interface**](ijournalreader.md)
</dt> <dt>

[Referência de esquema de leitor de diário](journal-reader-schema-reference.md)
</dt> </dl>

 

 
