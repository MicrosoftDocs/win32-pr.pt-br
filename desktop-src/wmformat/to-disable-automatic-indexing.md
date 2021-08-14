---
title: Para desabilitar a indexação automática
description: Para desabilitar a indexação automática
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows SDK do formato de mídia, desabilitando a indexação automática
- Windows SDK do formato de mídia, indexação automática
- ASF (Advanced Systems Format), desabilitando a indexação automática
- ASF (formato de sistemas avançados), desabilitando a indexação automática
- ASF (Advanced Systems Format), indexação automática
- ASF (formato de sistemas avançados), indexação automática
- índices, desabilitando a indexação automática
- índices, indexação automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3b63d58b8f9a0fbbdff88369832b67abca7d9f11a39c56613c6e5d867d6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699906"
---
# <a name="to-disable-automatic-indexing"></a>Para desabilitar a indexação automática

Talvez nem sempre você queira que um índice seja gerado por padrão ao gravar um arquivo ASF. Você pode desabilitar a indexação automática usando o método [**IWMWriterFileSink3:: SetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing) .

O código de exemplo a seguir demonstra como desabilitar a indexação automática pelo gravador.


```C++
IWMWriterFileSink*  pBaseFileSink = NULL;
IWMWriterFileSink3* pMySink       = NULL;

BOOL    fAutoIndex;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer file sink.
hr = WMCreateWriterFileSink(&pBaseFileSink);

// Retrieve an IWMWriterFileSink3 interface pointer for the new sink.
hr = pBaseFileSink->QueryInterface(IID_IWMWriterFileSink3,
                                    (void**)&pMySink);

// Release the base file sink.
pBaseFileSink->Release();
pBaseFileSink = NULL;

// Check the state of automatic indexing.
hr = pMySink->GetAutoIndexing(&fAutoIndex);

// If auto indexing is enabled, turn it off.
if(fAutoIndex)
   pMySink->SetAutoIndexing(FALSE);

// You can now write to this sink and the file will not have an index.

// Release the remaining interface.
pMySink->Release();
pMySink = NULL;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriterFileSink3::GetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




