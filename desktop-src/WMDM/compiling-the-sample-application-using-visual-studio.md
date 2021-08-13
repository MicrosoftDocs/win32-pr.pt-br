---
title: Compilando o aplicativo de exemplo usando Visual Studio
description: Compilando o aplicativo de exemplo usando Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Windows Mídia Gerenciador de Dispositivos, exemplos
- Gerenciador de Dispositivos,exemplos
- aplicativos da área de trabalho, exemplos
- Windows Mídia Gerenciador de Dispositivos, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos exemplo de aplicativo da área de trabalho
- exemplos, aplicativos da área de trabalho
- exemplos, compilando usando Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8b32cd5931a88bc41b8eee7171b6ab4ab18b629a8108007d68094180efaa77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586247"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Compilando o aplicativo de exemplo usando Visual Studio

O SDK Windows Media Gerenciador de Dispositivos inclui uma solução Visual Studio que é compatível com Microsoft Visual Studio 2005.

Antes de compilar o aplicativo de exemplo, você deve renomear o arquivo de header shtypes.h para evitar conflitos com um arquivo com o mesmo nome encontrado no SDK da Plataforma da Microsoft. Por exemplo, você pode renomear o caminho de instalação do *SDK* do <> \\ WMFSDK11 incluindo shtypes.h para o caminho de instalação do \\ \\ *SDK* do <> \\ WMFSDK11 incluir \\ \\ shtypes.h.backup.

Para criar o aplicativo, inicie uma instância do Visual Studio 2005, abra o arquivo de solução wmdmapp.sln, que é encontrado na pasta caminho de instalação do *SDK* do <> \\ Aplicativos WMFSDK11 wmdmapp e escolha a opção \\ \\ **Criar/Criar** Solução. Isso criará dois arquivos de projeto: o projeto auxiliar, proghelp.vcproj, bem como o aplicativo principal wmdmapp.vcproj. Além disso, ele criará a DLL auxiliar de progresso e o aplicativo principal (WMDMApp.exe).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Aplicativo de área de trabalho de exemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




