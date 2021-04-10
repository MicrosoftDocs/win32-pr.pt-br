---
description: A API de tíquete de impressão fornece permite que os aplicativos gerenciem e convertam os tíquetes de impressão.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API de tíquete de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011966"
---
# <a name="print-ticket-api"></a>API de tíquete de impressão

A API de tíquete de impressão fornece permite que os aplicativos gerenciem e convertam os tíquetes de impressão.

Um tíquete de impressão é um componente de documento XPS que contém as configurações de impressora preferenciais para uma página em um documento, ou para um documento inteiro ou para um trabalho de impressão que contenha um ou mais documentos. Observe que os tíquetes de impressão só são encontrados em documentos XPS.

Antes que a impressora possa usar o tíquete de impressão, o tíquete de impressão deve ser validado em relação às características da impressora, que são definidas nos recursos de impressão da impressora. O aplicativo executa essa validação chamando a API de tíquete de impressão.

Os PrintTicket e PrintCapabilities são descritos usando elementos do esquema de impressão, que é definido pela [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Este tópico contém informações sobre os seguintes elementos de API:

-   [Funções da API de tíquete de impressão](print-ticket-api-functions.md)
-   [Enumerações de API de tíquete de impressão](print-ticket-api-enumerations.md)

O diagrama a seguir mostra a relação da API de tíquete de impressão com as outras APIs de impressão que um aplicativo nativo do Windows pode usar.

![um diagrama que mostra a relação da API de tíquete de impressão com outras APIs de impressão que um aplicativo nativo do Windows pode usar](images/print-apis-pt.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de impressão XPS](xps-printing.md)
</dt> <dt>

[API do spooler de impressão](print-spooler-api.md)
</dt> <dt>

[API de impressão GDI](gdi-printing.md)
</dt> <dt>

[Especificação de esquema de impressão](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[Especificação de Papel XML](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



