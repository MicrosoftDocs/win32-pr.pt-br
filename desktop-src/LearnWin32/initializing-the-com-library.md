---
title: Inicializando a biblioteca COM
description: Inicializando a biblioteca COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1bc9536c186c2af3b604f7eb5666a6a31e7a845cf3b20f64a132119d16cb1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979986"
---
# <a name="initializing-the-com-library"></a>Inicializando a biblioteca COM

Qualquer Windows que usa COM deve inicializar a biblioteca COM chamando a [**função CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Cada thread que usa uma interface COM deve fazer uma chamada separada para essa função. **CoInitializeEx** tem a seguinte assinatura:


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



O primeiro parâmetro é reservado e deve ser **NULL.** O segundo parâmetro especifica o modelo de threading que seu programa usará. O COM dá suporte a dois modelos de threading diferentes, *apartment threaded* *e multithreaded.* Se você especificar o threading de apartment, você está fazendo as seguintes garantias:

-   Você acessará cada objeto COM de um único thread; você não compartilhará ponteiros de interface COM entre vários threads.
-   O thread terá um loop de mensagem. (Consulte [Mensagens da Janela](window-messages.md) no Módulo 1.)

Se qualquer uma dessas restrições não for verdadeira, use o modelo multithread. Para especificar o modelo de threading, de definir um dos sinalizadores a seguir no *parâmetro dwCoInit.*



| Sinalizador                          | Descrição         |
|-------------------------------|---------------------|
| **COINIT \_ APARTMENTTHREADED** | Apartment threaded. |
| **COINIT \_ MULTITHREADED**     | Multithread.      |



 

Você deve definir exatamente um desses sinalizadores. Em geral, um thread que cria uma janela deve usar o sinalizador **COINIT \_ APARTMENTTHREADED** e outros threads devem usar **COINIT \_ MULTITHREADED**. No entanto, alguns componentes COM exigem um modelo de threading específico. A documentação do MSDN deve dizer quando esse é o caso.

> [!Note]  
> Na verdade, mesmo que você especifique o threading de apartment, ainda é possível compartilhar interfaces entre threads usando uma técnica chamada *marshaling*. O marshaling está além do escopo deste módulo. O ponto importante é que, com o threading de apartment, você nunca deve simplesmente copiar um ponteiro de interface para outro thread. Para obter mais informações sobre os modelos de threading COM, consulte [Processos, threads e apartments.](/windows/desktop/com/processes--threads--and-apartments)

 

Além dos sinalizadores já mencionados, é uma boa ideia definir o sinalizador **COINIT \_ DISABLE \_ OLE1DDE** no *parâmetro dwCoInit.* Definir esse sinalizador evita alguma sobrecarga associada à OLE (Vinculação e Incorporação de Objetos) 1.0, uma tecnologia obsoleta.

Veja como você inicializaria COM para threading de apartment:


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



O **tipo de retorno HRESULT** contém um código de erro ou êxito. Vamos ver o tratamento de erro COM na próxima seção.

## <a name="uninitializing-the-com-library"></a>Como não reinicializar a biblioteca COM

Para cada chamada bem-sucedida para [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), você deve chamar [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) antes que o thread saia. Essa função não tem parâmetros e não tem nenhum valor de retorno.


```C++
CoUninitialize();
```



## <a name="next"></a>Avançar

[Códigos de erro em COM](error-codes-in-com.md)

 

 