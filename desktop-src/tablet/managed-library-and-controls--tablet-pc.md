---
description: Para criar aplicativos de Tablet PC em C e Visual Basic .NET Microsoft Visual Studio, seu projeto no .NET deve incluir uma referência aos assemblies da biblioteca gerenciada \# do tablet PC. Isso fornece acesso aos controles e ao modelo de objeto gerenciado.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Biblioteca e controles gerenciados (tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d031a97226d200b99a6d36b42e3e4c43862f5b6ac52203ee4ca08d1e5714f2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031724"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Biblioteca e controles gerenciados (tablet PC)

Para criar aplicativos de Tablet PC em C e Visual Basic .NET Microsoft Visual Studio, seu projeto no .NET deve incluir uma referência aos assemblies da biblioteca gerenciada \# do tablet PC. Isso fornece acesso aos controles e ao modelo de objeto gerenciado.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# e Visual Basic.NET

No Windows Vista, os assemblies da biblioteca gerenciada de tablet pc são instalados por padrão em dois diretórios:

-   <systemdrive>: \\ Diretório de Arquivos Comuns de Arquivos Comuns da Microsoft Shared \\ \\ \\ Ink
-   <systemdrive>: \\ Arquivos de Programas microsoft \\ SDKs \\ Windows \\ v6.0 \\ Bin

Para adicionar uma referência às bibliotecas gerenciadas da plataforma tablet pc no Microsoft Visual Studio .NET:

1.  Abra seu Visual Studio .NET.
2.  No menu **Projeto**, clique em **Adicionar Referência**.
3.  Na guia **.NET** na caixa **de diálogo Adicionar Referência,** na lista de componentes, selecione **API de PC do Microsoft Tablet**.
4.  Clique **em Selecionar** e, em seguida, clique em **OK.**

Para adicionar uma referência às APIs de análise de tinta Visual Studio .NET:

1.  Abra seu Microsoft Visual Studio .NET.
2.  No menu **Projeto**, clique em **Adicionar Referência**.
3.  Na guia **.NET na** caixa **de diálogo Adicionar Referência,** na lista de componentes, selecione **Biblioteca Gerenciada** de Análise de Tinta do Pc tablet da Microsoft.
4.  Clique **em Selecionar** e, em seguida, clique em **OK.**

> [!Note]  
> Ao compilar aplicativos que usam o Microsoft.Ink no Visual Studio 2005, você deve selecionar **Project**, selecionar Propriedades **,** selecionar **Compilar** e definir Platform target=x86. Essa opção não está disponível em Microsoft Visual Studio Express produtos.

 

 

 



