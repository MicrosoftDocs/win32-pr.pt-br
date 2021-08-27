---
description: Explore as tecnologias relacionadas ao esquema de impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: Schema-Related tecnologias de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2948108b8bd6f581608471c9646fe135f83cb91561dc3c4cca97ac4df10560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112266"
---
# <a name="print-schema-related-technologies"></a>Schema-Related tecnologias de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

para o .NET Framework 3,0, Windows Vista e versões posteriores, as tecnologias de printcapabilities e PrintTicket estendem os recursos do esquema de impressão para permitir uma experiência de impressão mais rica.

## <a name="printcapabilities"></a>PrintCapabilities

A tecnologia PrintCapabilities é um método de publicação de configurações controláveis do usuário para a descrição de atributos e configurações por trabalho. As PrintCapabilities são publicadas em um documento XML chamado documento de PrintCapabilities, que consiste em termos definidos nas palavras-chave do esquema de impressão e nas extensões privadas. O documento PrintCapabilities pode ser considerado como um "instantâneo" da configuração do dispositivo atual de estado configurável pelo usuário, bem como uma descrição de possíveis configurações. Dispositivos (ou drivers de dispositivo) geram um documento de PrintCapabilities (o instantâneo) de seu conjunto atual de opções configuráveis quando consultados por clientes, que podem ser aplicativos ou o subsistema de impressão. Este documento descreve todos os recursos de PrintCapabilities configuráveis disponíveis no dispositivo, como opções de acabamento e opções de layout de página. O documento PrintCapabilities descreve explicitamente todos os atributos do dispositivo e as configurações permitidas para cada atributo. Com o uso da estrutura de esquema de impressão, os atributos de dispositivo podem ser precisamente descritos e comparados com eficiência. Usando as palavras-chave contidas no documento de palavras-chave do esquema de impressão e a estrutura definida na estrutura de esquema de impressão, os dispositivos podem permitir que os clientes usem com mais eficiência os PrintCapabilities. Para obter mais informações, consulte [criação de esquema e documento de PrintCapabilities](printcapabilities-schema-and-document-construction.md).

em relação ao subsistema de impressão no Microsoft Windows Server 2003 e anterior, a tecnologia printcapabilities permite que os componentes de subsistema de cliente e impressão exibam de modo transparente as informações contidas nos recursos binários do sistema Win32 atuais. Isso permite que o cliente consulte recursos de PrintCapabilities, receba um instantâneo XML consistente e bem compreendido e use-o para construir um PrintTicket para um dispositivo sem invocar a interface do usuário do driver.

## <a name="printticket"></a>PrintTicket

A tecnologia PrintTicket é a sucessora da estrutura DEVMODE atual. É um documento baseado em linguagem de marcação extensível que especifica e mantém informações sobre a formatação do trabalho e a configuração do trabalho de impressão. Uma instância do PrintTicket atribui configurações de dispositivo específicas e transmite a intenção do usuário. Há dois tipos de PrintTicket: PrintTickets genéricos, que não são gerados para um dispositivo específico; e os PrintTickets específicos do dispositivo, que são construídos para um dispositivo específico. Os PrintTickets genéricos, que se destinam a serem portáteis em dispositivos, derivam seu conteúdo selecionando configurações para cada um dos atributos de dispositivo descritos exclusivamente nas palavras-chave do esquema de impressão. Os PrintTickets específicos do dispositivo derivam seu conteúdo de um documento de PrintCapabilities, selecionando configurações para cada atributo de dispositivo anunciado por este documento. Esses PrintTickets também podem incluir extensões privadas, específicas para um modelo de dispositivo ou família de modelos de dispositivo. Para obter mais informações, consulte [construção de esquema e documento do PrintTicket](printticket-schema-and-document-construction.md).

Em relação ao subsistema de impressão atual, a tecnologia PrintTicket permite que todos os componentes e clientes do subsistema de impressão tenham acesso transparente às informações atualmente armazenadas nas partes públicas e privadas da estrutura DEVMODE, usando um formato XML bem definido. Esse design resolve problemas atuais encontrados em cenários de atualização de driver ou de desigualdade de driver em drivers projetados para a tecnologia PrintTicket. Atualmente, esses cenários podem resultar em uma perda de configurações e, portanto, uma experiência de cliente negativa. O PrintTicket também permite novos cenários, como habilitar um driver de impressora para expor suas configurações de DEVMODE privado para aplicativos e plug-ins personalizados de maneira consistente e inequívoca. Isso permite que os componentes de impressão sejam mais transparentes e manipulem as migrações de configurações com mais clareza. As interfaces PrintTicket serão expostas aos aplicativos por meio de métodos em objetos de código gerenciado que também estarão disponíveis para scripts. na nova estrutura de aplicativos criada em objetos de código gerenciado no .NET Framework 3,0, o PrintTicket é a maneira padrão de descrever as configurações do documento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



