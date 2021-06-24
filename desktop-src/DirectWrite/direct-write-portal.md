---
title: DirectWrite (DWrite)
description: Os aplicativos atuais devem dar suporte à renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução e suporte completo a texto e layout Unicode. O DirectWrite, uma API do [DirectX](../directx.md) , fornece esses recursos e muito mais.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587947"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Finalidade

Os aplicativos atuais devem dar suporte à renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução e suporte completo a texto e layout Unicode. O DirectWrite, uma API do [DirectX](../directx.md) , fornece esses recursos e muito mais.

- Um sistema de layout de texto independente de dispositivo que melhora a legibilidade do texto em documentos e na interface do usuário.
- Renderização de texto de alta qualidade e subpixel [do Microsoft ClearType](/typography/cleartype/) que pode usar a tecnologia de renderização [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)ou específica do aplicativo.
- Texto acelerado por hardware, quando usado com [Direct2D](rendering-by-using-direct2d.md).
- Suporte para texto de vários formatos.
- Suporte para os recursos de tipografia avançada de fontes OpenType.
- Suporte para layout e renderização de texto em todos os idiomas com suporte.
- Layout e renderização compatíveis com [GDI](interoperating-with-gdi.md).

A API dá suporte à medição, ao desenho e ao teste de impacto de texto de vários formatos. O DirectWrite lida com o texto em todos os idiomas com suporte para aplicativos globais e localizados, criando a infraestrutura de linguagem principal encontrada no Windows 7. O DirectWrite também oferece uma API de renderização de glifos de nível inferior para desenvolvedores que queiram executar seu próprio processamento Unicode em glifo.

> [!NOTE]
> O [SDK de aplicativos do Windows](/windows/apps/windows-app-sdk/) introduz uma nova versão do DirectWrite &mdash; chamada DWriteCore &mdash; , que é executada em versões do Windows até o Windows 8, e abre a porta para você usá-la entre plataformas. Para obter mais detalhes, consulte [visão geral do DWriteCore](dwritecore-overview.md).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

- Windows 7 ou Windows Vista com Service Pack 2 (SP2) e atualização de plataforma para Windows Vista
- Windows Server 2008 R2 ou Windows Server 2008 com Service Pack 2 (SP2) e atualização de plataforma para Windows Server 2008

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [O que há de novo no DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Aqui estão algumas das novas adições ao DirectWrite. <br/> |
| [Guia de programação](programming-guide.md)<br/> | Os tópicos a seguir fornecem uma visão geral da API do DirectWrite.<br/> |
| [Referência da API](reference.md)<br/> | Descreve a API do DirectWrite.<br/> |
| [Código de exemplo](samples.md)<br/> | Esta seção contém informações sobre programas de exemplo para DirectWrite.<br/> |
