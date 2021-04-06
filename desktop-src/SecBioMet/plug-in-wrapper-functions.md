---
title: Funções de wrapper de plug-in
description: Funções de wrapper que permitem chamar uma função pública em qualquer adaptador anexado ao pipeline sem adquirir manualmente um ponteiro para o adaptador.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- API de Windows Biometric Framework de API Windows Biometric Framework, funções de wrapper de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822915"
---
# <a name="plug-in-wrapper-functions"></a>Funções de wrapper de plug-in

A API de Windows Biometric Framework inclui funções de wrapper que permitem chamar uma função pública em qualquer adaptador anexado ao pipeline sem adquirir manualmente um ponteiro para o adaptador. Cada wrapper verifica os argumentos de entrada, recupera um ponteiro de adaptador e chama a função solicitada. Por exemplo, o wrapper **WbioEngineSetHashAlgorithm** tem a assinatura a seguir.


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



A função verifica se o argumento de *pipeline* não é **nulo**, se existe um adaptador de mecanismo e se a função [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) existe. Todas as funções de wrapper são definidas no \_ arquivo de cabeçalho WinBio Adapter. h. Os tópicos a seguir discutem os wrappers disponíveis.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                               | Descrição                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Wrappers do adaptador do mecanismo](engine-adapter-wrappers.md)<br/>   | Funções que você pode usar para chamar funções em seu adaptador de mecanismo. Essas funções são definidas em WinBio \_ Adapter. h.<br/>  |
| [Wrappers do adaptador do sensor](sensor-adapter-wrappers.md)<br/>   | Funções que você pode usar para chamar funções no adaptador do sensor. Essas funções são definidas em WinBio \_ Adapter. h.<br/>  |
| [Wrappers do adaptador de armazenamento](storage-adapter-wrappers.md)<br/> | Funções que você pode usar para chamar funções em seu adaptador de armazenamento. Essas funções são definidas em WinBio \_ Adapter. h.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de plug-in](plug-in-reference.md)
</dt> </dl>

 

 





