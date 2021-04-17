---
description: Criando aplicativos do DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Criando aplicativos do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812766"
---
# <a name="building-directshow-applications"></a>Criando aplicativos do DirectShow

Este tópico descreve os cabeçalhos e as bibliotecas necessárias para criar aplicativos do DirectShow.

Os cabeçalhos e as bibliotecas do DirectShow mais recentes estão disponíveis na [SDK do Windows](https://msdn.microsoft.com/windows/aa904949.aspx).

## <a name="header-files"></a>Arquivos de cabeçalho

Todos os aplicativos do DirectShow usam o arquivo de cabeçalho mostrado na tabela a seguir.



| Arquivos de cabeçalho | Necessário para                 |
|-------------|------------------------------|
| DShow. h     | Todos os aplicativos do DirectShow. |



 

Algumas interfaces do DirectShow exigem arquivos de cabeçalho adicionais. Esses requisitos são indicados na referência de interface.

## <a name="library-files"></a>Arquivos de biblioteca

O DirectShow usa os arquivos de biblioteca estática mostrados na tabela a seguir.



| Arquivo de biblioteca | Descrição                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| Strmiids. lib | Exporta identificadores de classe (CLSIDs) e identificadores de interface (IIDs).                                                           |
| Quartz. lib   | Exporta a função [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) . Se você não chamar essa função, essa biblioteca não será necessária. |



 

Use os mesmos arquivos. lib para compilações de depuração e versão.

## <a name="filter-base-classes"></a>Filtrar classes base

O SDK do Windows fornece um conjunto de classes C++ que são recomendadas se você estiver escrevendo um filtro DirectShow personalizado. Essas classes são fornecidas como um código de exemplo, que você pode compilar em uma biblioteca estática. Para obter mais informações, consulte [classes base do DirectShow](directshow-base-classes.md).

## <a name="redistributable-dlls"></a>DLLs redistribuíveis

Os aplicativos do DirectShow escritos para o Windows XP com Service Pack 2 (SP2) e posterior não precisam redistribuir as DLLs do DirectShow.

Para o Windows XP com Service Pack 1 (SP1) e versões anteriores, as DLLs do DirectShow redistribuíveis estão disponíveis no SDK do Microsoft DirectX. A versão mais recente dessas DLLs é a versão 9.0 c. Não é planejado nenhum desenvolvimento adicional dessas DLLs redistribuíveis. O Windows XP com Service Pack 2 (SP2) contém as DLLs da versão 9.0 c.

Os pacotes redstributable contêm as seguintes DLLs:

-   dxnt.cab
    -   amstream.dll
    -   devenum.dll
    -   encapi.dll
    -   ks.sys
    -   ksolay.ax
    -   ksproxy.ax
    -   ksuser.dll
    -   l3codecx.ax
    -   mciqtz32.dll
    -   mpg2splt.ax
    -   msdmo.dll
    -   mskssrv.sys
    -   mspclock.sys
    -   mspqm.sys
    -   mstee.sys
    -   mswebdvd.dll
    -   qasf.dll
    -   qcap.dll
    -   qdv.dll
    -   qdvd.dll
    -   qedit.dll
    -   qedwipes.dll
    -   quartz.dll
    -   stream.sys
    -   swenum.sys
-   bda.cab
    -   bdaplgin.ax
    -   bdasup.sys
    -   ccdecode.sys
    -   ipsink.ax
    -   kstvtune.ax
    -   kswdmcap.ax
    -   ksxbar.ax
    -   mpe.sys
    -   mpeg2data.ax
    -   msdv.sys
    -   msdvbnp.ax
    -   msvidctl.dll
    -   msyuv.dll
    -   nabtsfec.sys
    -   ndisip.sys
    -   psisdecd.dll
    -   psisrndr.ax
    -   slip.sys
    -   streamip.sys
    -   vbisurf.ax
    -   wstcodec.sys
    -   wstdecod.dll

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando filtros do DirectShow](building-directshow-filters.md)
</dt> </dl>

 

 
