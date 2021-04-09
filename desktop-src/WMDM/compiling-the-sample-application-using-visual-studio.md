---
title: Compilando o aplicativo de exemplo usando o Visual Studio
description: Compilando o aplicativo de exemplo usando o Visual Studio
ms.assetid: 78345cdb-5f0d-4ea8-9492-30386f5fa6ee
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- aplicativos de área de trabalho, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos, exemplo de aplicativo de desktop
- exemplos, aplicativos de desktop
- exemplos, compilando usando o Visual Studio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf47f7a45ad17711145df810926fafb0f2aedcec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005288"
---
# <a name="compiling-the-sample-application-using-visual-studio"></a>Compilando o aplicativo de exemplo usando o Visual Studio

O SDK do Windows Media Gerenciador de Dispositivos inclui uma solução do Visual Studio que é compatível com o Microsoft Visual Studio 2005.

Antes de compilar o aplicativo de exemplo, você deve renomear o arquivo de cabeçalho shtypes. h para evitar conflitos com um arquivo com o mesmo nome encontrado no SDK da plataforma Microsoft. Por exemplo, você pode renomear <*caminho de instalação do SDK* > \\ WMFSDK11 \\ incluir \\ shtypes. h para <*caminho de instalação do SDK* > \\ WMFSDK11 \\ incluir \\ shtypes. h. backup.

Para compilar o aplicativo, inicie uma instância do Visual Studio 2005, abra o arquivo de solução, wmdmapp. sln, que está localizado na pasta <*caminho de instalação do SDK* > \\ WMFSDK11 \\ aplicativos \\ wmdmapp e escolha a opção de **solução compilar/compilar** . Isso criará dois arquivos de projeto: o projeto auxiliar, proghelp. vcproj, bem como o aplicativo principal wmdmapp. vcproj. Além disso, ele criará a DLL auxiliar de progresso e o aplicativo principal (WMDMApp.exe).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Aplicativo de desktop de exemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




