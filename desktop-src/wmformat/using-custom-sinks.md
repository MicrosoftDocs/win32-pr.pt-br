---
title: Usando coletores personalizados
description: Usando coletores personalizados
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- ASF (Advanced Systems Format), coletores personalizados
- ASF (formato de sistemas avançados), coletores personalizados
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, coletores personalizados
- coletores personalizados, sobre
- coletores de gravador, coletores personalizados
- coletores personalizados, interface IWMWriterSink
- IWMWriterSink
- coletores de gravador, interface IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640141"
---
# <a name="using-custom-sinks"></a>Usando coletores personalizados

Se você tiver uma necessidade de gravação especial, poderá criar seus próprios coletores de gravador. O gravador mantém uma comunicação unidirecional com um coletor fazendo chamadas para os métodos de [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink). Para criar seu próprio coletor, implemente a interface **IWMWriterSink** em uma classe em seu aplicativo. Esse processo é muito semelhante à implementação de qualquer outra interface de retorno de chamada usada pelos objetos do SDK do Windows Media Format. Para obter mais informações sobre retornos de chamada, consulte [usando os métodos de retorno de chamada](using-the-callback-methods.md).

O buffer recebido em [**IWMWriterSink:: Onheader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) deve ser gravado no início do arquivo e todos os buffers recebidos em [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) devem ser gravados em sequência. O **Onheader** será chamado no início, mas pode ser chamado em outras ocasiões também e, se for, você deverá, se possível, substituir o cabeçalho original. Se o seu aplicativo não puder fazer isso por algum motivo, simplesmente ignore as chamadas de **Onheader** subsequentes.

Seu coletor personalizado deve comunicar seu status ao aplicativo de gravação fazendo chamadas para o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Se você implementar o coletor como um objeto COM, talvez queira expor a interface [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) . No entanto, você pode passar o endereço do retorno de chamada **OnStatus** para o coletor e definir um contexto da maneira que desejar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> </dl>

 

 




