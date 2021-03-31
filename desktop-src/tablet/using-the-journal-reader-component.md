---
description: O componente leitor de notas do diário do Microsoft Windows fornece acesso de leitura programático a arquivos no formato de diário.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Usando o componente de leitor de diário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920878"
---
# <a name="using-the-journal-reader-component"></a>Usando o componente de leitor de diário

O componente leitor de notas do diário do Microsoft Windows fornece acesso de leitura programático a arquivos no formato de diário.

## <a name="component-overview"></a>Visão geral do componente

Os arquivos de diário têm a extensão de arquivo. jnt. Esse componente simples usa um fluxo que contém um arquivo. jnt e retorna um fluxo que contém o conteúdo do arquivo em formato XML. O XML retornado pelo componente está de acordo com o esquema de leitor de nota do diário. Esse esquema está documentado na [referência de esquema do leitor de diário](journal-reader-schema-reference.md).

O componente não fornece a capacidade de gravar arquivos. jnt.

O componente está disponível em versões não gerenciadas e gerenciadas. O componente não gerenciado está disponível no journal.dll biblioteca de vínculo dinâmico (DLL). A versão gerenciada está no assembly Microsoft.Ink.Journal.dll (para redistribuição para o Windows XP Tablet PC Edition ou Windows Vista) ou Microsoft.Ink.dll.

> [!IMPORTANT]
>
> A partir do Windows 10, versão 1607, o journal.dll não está incluído no sistema operacional Windows. Essa biblioteca deve ser considerada preterida ou obsoleta e não deve ser usada.

 

### <a name="assembly-changes-of-note"></a>Alterações de assembly de observação

É importante estar ciente de algumas alterações no assembly que contêm o componente de leitor de nota do diário que ocorreu entre a versão lançada em conjunto com a versão 1,7 do kit de desenvolvedores de Tablet e a versão fornecida no sistema operacional Windows Vista.

A versão 1,7 do componente de leitor, que pode ser redistribuído para o Windows XP ou o Windows Vista, está contida em um assembly chamado Microsoft.Ink.Journal.dll. O componente de leitor é fornecido no Windows Vista, mas foi integrado ao assembly de Microsoft.Ink.dll principal. Isso significa que os aplicativos que fazem uso do assembly 1,7 precisam redistribuir esse assembly com a configuração.

## <a name="using-the-component"></a>Usando o componente

O componente leitor de nota do diário é útil para extrair os dados de tinta e outras informações sobre o arquivo de um arquivo de diário.

### <a name="com"></a>COM

O componente COM do leitor de anotações do diário está no arquivo Journal.dll, que é instalado e registrado quando você baixa e executa o arquivo de instalação do leitor de notas do diário.

O componente COM não oferece suporte à interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .

### <a name="managed"></a>Gerenciado

O componente gerenciado do leitor de anotações do diário está no assembly Microsoft.Ink.JournalReader.dll. Esse assembly é instalado e registrado no cache de assembly global quando você executa o arquivo de instalação do leitor de notas do diário.

Adicione uma referência ao assembly para usá-lo em seu projeto gerenciado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IJournalReader**](ijournalreader.md)
</dt> <dt>

[Referência de esquema do leitor de diário](journal-reader-schema-reference.md)
</dt> </dl>

 

 
