---
title: Personalizar uma miniatura icônica e um bitmap de versão prévia dinâmica
description: Mostra como personalizar uma miniatura de icônico e um bitmap de visualização dinâmica (também chamado de visualização de inspeção).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105787670"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a>Personalizar uma miniatura icônica e um bitmap de versão prévia dinâmica

## <a name="description"></a>Descrição

Você pode personalizar uma miniatura de icônico e um bitmap de *Visualização dinâmica* (ou *visualização de inspeção*) usando funções e mensagens que são introduzidas nas APIs do Windows 7 Gerenciador de janelas da área de trabalho (DWM).

Especificamente, você usa a função [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) e a [**mensagem \_ SENDICONICTHUMBNAILBITMAP do WM**](wm-dwmsendiconicthumbnail.md) para personalizar uma miniatura icônico. Você também pode usar a função [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) e a mensagem do [**WM \_ SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) para definir um bitmap de visualização dinâmica do icônico.

Para um aplicativo de exemplo que usa a função **DwmSetIconicThumbnail** , consulte o [exemplo TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).

A ilustração a seguir mostra uma miniatura padrão transformada em uma miniatura personalizada.

![ilustração de uma imagem em miniatura original e uma imagem em miniatura modificada com um bitmap personalizado](images/customthumbnail.jpg)

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 7 ou Windows Vista com Service Pack 2 (SP2) e atualização de plataforma para Windows Vista                          |
| Servidor mínimo com suporte | Windows Server 2008 R2 ou Windows Server 2008 com Service Pack 2 (SP2) e atualização de plataforma para Windows Server 2008 |
| SDK do Windows mínimo      | [SDK (Software Development Kit) do Windows para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a>Criando o exemplo de TabThumbnails

**Para compilar o exemplo usando Microsoft Visual Studio (método preferencial)**

1.  Abra o Windows Explorer e navegue até a pasta onde o arquivo TabThumbnails. sln está localizado.
2.  Clique duas vezes no arquivo de solução (. sln) para abrir o arquivo em Microsoft Visual Studio.
3.  No menu **Compilar**, clique em **Compilar Solução**. O aplicativo é criado no diretório de \\ depuração ou de \\ lançamento padrão.

**Para criar o exemplo usando o prompt de comando**

1.  Abra uma janela de prompt de comando e navegue até o diretório de exemplo.
2.  Digite `msbuild TabThumbnails.sln`.

## <a name="related-topics"></a>Tópicos relacionados

[Gerenciador de Janelas da Área de Trabalho](dwm-overview.md)

[Desenvolvimento em Windows](/windows/desktop/win32-and-com-development)
