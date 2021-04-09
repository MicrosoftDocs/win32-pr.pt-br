---
title: Documentos e periféricos do documento
description: O Windows 7 fornece aos desenvolvedores uma plataforma robusta para trabalhar com documentos e integrar periféricos de documentos.
ms.assetid: 77d27775-eea8-4739-a1d2-05fcf6590cef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e220949d37c17b95f92ed5026166ea71043354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007951"
---
# <a name="documents-and-document-peripherals"></a>Documentos e periféricos do documento

O Windows 7 fornece aos desenvolvedores uma plataforma robusta para trabalhar com documentos e integrar periféricos de documentos. Duas novas tecnologias de documento e armazenamento foram introduzidas no Windows Vista: a XPS (XML Paper Specification) e o OPC (Open Packaging Conventions). Essas tecnologias, que estavam disponíveis no Windows Vista somente para desenvolvedores de aplicativos de código gerenciado por meio do Microsoft .NET Framework, agora estão disponíveis no SDK (Kit de desenvolvimento 7software) do Windows para uso por desenvolvedores de código não gerenciado.

## <a name="open-packaging-conventions"></a>Open Packaging Conventions

O Windows 7 oferece suporte a todos os formatos de arquivo OPC, incluindo aqueles da Microsoft, bem como aqueles de terceiros. O OPC é um componente da especificação internacional do Office Open XML (OOXML) definida por meio de *ISO/IEC DIS 29500* e *ECMA-376*. Com base no formato de arquivo *zip* , o OPC permite que os aplicativos armazenem uma combinação de itens de dados em um único arquivo de pacote. Os desenvolvedores de aplicativos podem usar as APIs de *empacotamento* no Windows 7 para criar, ler e manipular vários elementos de dados em arquivos baseados em OPC.

Usando as APIs de *empacotamento* no Windows 7, os desenvolvedores podem criar novos formatos de pacote para acomodar os requisitos de armazenamento de dados específicos do aplicativo.

As assinaturas digitais *X509* também têm suporte nas APIs de *empacotamento*. Os desenvolvedores podem usar os recursos de assinatura digital para assinar e validar partes selecionadas de um pacote OPC ou todo o pacote. Os aplicativos podem dar a seus documentos um nível de segurança adicional usando assinaturas digitais para detectar quando o conteúdo de um arquivo baseado em OPC foi alterado depois que o arquivo foi assinado. (Consulte [visão geral do Open Packaging Conventions](/previous-versions/windows/desktop/opc/open-packaging-conventions-overview).)

## <a name="xps-documents"></a>Documentos XPS

Os desenvolvedores de aplicativos do Windows podem criar aplicativos que produzem documentos XPS com o Windows 7. Isso permite que eles se integrem rigidamente ao ecossistema de periféricos de documentos (dispositivos como scanners e impressoras) e trabalhem com o papel eletrônico seguro para dar suporte à publicação e ao arquivamento.

Em versões anteriores do Windows, o XPS não tinha suporte para desenvolvedores do Microsoft Win32. O XPS foi introduzido no Windows Vista, mas a superfície de API era limitada a desenvolvedores de .NET que trabalham com código gerenciado. Com o Windows 7, os desenvolvedores do Win32 podem usar as novas APIs de *documento* XPS para reduzir a quantidade de trabalho necessária ao trabalhar com o XPS. Como o XPS é a base para a nova plataforma de impressão do Windows, esse é um benefício significativo.

Nas versões anteriores do Windows, o acesso ao caminho de impressão XPS de aplicativos Win32 era limitado a escapes de driver. Isso reduziu significativamente o utilitário do caminho de impressão para os desenvolvedores que não usam código gerenciado. Para desenvolvedores do Win32, a nova API de *impressão* XPS reduz significativamente a quantidade de trabalho necessária para se beneficiar das vantagens do caminho de impressão do XPS e elimina a necessidade de código de impressão paralelo.

Os desenvolvedores de aplicativos podem usar documentos XPS para compartilhar e arquivar conteúdo como papel eletrônico em um formato de alta fidelidade, eficiente e confiável. Assim como o Windows Vista, o caminho de impressão no Windows 7 foi criado com base no formato XPS para fornecer recursos de impressão aprimorados. As APIs de documento XPS no Windows 7 oferecem aos desenvolvedores a capacidade de criar, acessar e manipular documentos XPS facilmente. (Consulte o [Guia de programação de documento XPS](/previous-versions//dd372978(v=vs.85)).)

![Visualizador XPS](images/windows7-devguide-xpsviewer.jpg)

Os desenvolvedores de aplicativos do Windows podem criar aplicativos que produzem documentos XPS com o Windows 7

 

 