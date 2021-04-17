---
description: Para criar aplicativos de Tablet PC em C \# e Visual Basic .net, seu projeto no Microsoft Visual Studio .NET deve incluir uma referência aos assemblies da biblioteca gerenciada do Tablet PC. Isso fornece acesso ao modelo de objeto gerenciado e aos controles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Biblioteca gerenciada e controles (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768303"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Biblioteca gerenciada e controles (Tablet PC)

Para criar aplicativos de Tablet PC em C \# e Visual Basic .net, seu projeto no Microsoft Visual Studio .NET deve incluir uma referência aos assemblies da biblioteca gerenciada do Tablet PC. Isso fornece acesso ao modelo de objeto gerenciado e aos controles.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# e visual Basic.net

No Windows Vista, os assemblies da biblioteca gerenciada do Tablet PC são instalados por padrão em dois diretórios:

-   <systemdrive>: \\ Arquivos de programas \\ Arquivos comuns \\ diretório de tinta compartilhada da Microsoft \\
-   <systemdrive>: \\ Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ bin

Para adicionar uma referência às bibliotecas gerenciadas da plataforma do Tablet PC no Microsoft Visual Studio .NET:

1.  Abra seu projeto do Visual Studio .NET.
2.  No menu **Projeto**, clique em **Adicionar Referência**.
3.  Na guia **.net** da caixa de diálogo **Adicionar referência** , na lista componentes, selecione **API do Microsoft Tablet PC**.
4.  Clique em **selecionar** e em **OK**.

Para adicionar uma referência às APIs de análise de tinta no Visual Studio .NET:

1.  Abra seu projeto Microsoft Visual Studio .NET.
2.  No menu **Projeto**, clique em **Adicionar Referência**.
3.  Na guia **.net** da caixa de diálogo **Adicionar referência** , na lista componentes, selecione **biblioteca gerenciada de análise de tinta do Microsoft Tablet PC**.
4.  Clique em **selecionar** e em **OK**.

> [!Note]  
> Ao compilar aplicativos que usam Microsoft. Ink no Visual Studio 2005, você deve selecionar **projeto**, selecionar **Propriedades**, selecionar **Compilar** e definir destino da plataforma = x86. Essa opção não está disponível em produtos Microsoft Visual Studio Express.

 

 

 



