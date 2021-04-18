---
description: MFTrace é uma ferramenta para gerar logs de rastreamento para aplicativos Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750180"
---
# <a name="mftrace"></a>MFTrace

MFTrace é uma ferramenta para gerar logs de rastreamento para aplicativos Media Foundation.

## <a name="in-this-section"></a>Nesta seção

-   [Usando MFTrace](using-mftrace.md)
-   [Palavras-chave MFTrace](mftrace-keywords.md)
-   [Arquivo de configuração MFTrace](mftrace-configuration-file.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------------------------------------------|
| Versão mínima do SDK      | SDK (Software Development Kit) do Microsoft Windows para Windows 7 e .NET Framework 4,0 |
| Sistema operacional mínimo | Windows Vista                                                                         |



 

O MFTrace requer as seguintes DLLs, que também são fornecidas no SDK.

-   detoured.dll
-   mfdetours.dll

O SDK fornece as versões de 32 bits e 64 bits do MFTrace. MFTrace não dá suporte a WOW64; para rastrear um processo de 32 bits em execução no Windows de 64 bits, use a versão de 32 bits do MFTrace.

SDK-raiz em sistemas de 32 bits: \Program Programas\windows Kits\10 SDK-root no sistema de 64 bits: \Program Files (x86) \Windows Kits\10 você encontrará mftrace no <SDK-root> \Bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de Media Foundation](media-foundation-tools.md)
</dt> </dl>

 

 



