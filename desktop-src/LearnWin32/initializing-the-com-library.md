---
title: Inicializando a biblioteca COM
description: Inicializando a biblioteca COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105780622"
---
# <a name="initializing-the-com-library"></a>Inicializando a biblioteca COM

Qualquer programa do Windows que usa COM deve inicializar a biblioteca COM chamando a função [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) . Cada thread que usa uma interface COM deve fazer uma chamada separada para essa função. **CoInitializeEx** tem a seguinte assinatura:


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



O primeiro parâmetro é reservado e deve ser **nulo**. O segundo parâmetro especifica o modelo de Threading que o programa usará. O COM dá suporte a dois modelos de Threading diferentes, *Apartment Threaded* e *multithread*. Se você especificar segmentação de apartamento, você está fazendo as seguintes garantias:

-   Você vai acessar cada objeto COM de um único thread; Você não compartilhará ponteiros de interface COM entre vários threads.
-   O thread terá um loop de mensagem. (Consulte [as mensagens de janela](window-messages.md) no módulo 1.)

Se uma dessas restrições não for verdadeira, use o modelo multi-threaded. Para especificar o modelo de Threading, defina um dos sinalizadores a seguir no parâmetro *dwCoInit* .



| Sinalizador                          | Descrição         |
|-------------------------------|---------------------|
| **APARTMENTTHREADED de coinicialização \_** | Apartment Threaded. |
| **coinit \_ multi-threaded**     | Multithread.      |



 

Você deve definir exatamente um desses sinalizadores. Geralmente, um thread que cria uma janela deve usar o sinalizador **coinit \_ APARTMENTTHREADED** e outros threads devem usar o **coinit \_ multi-threaded**. No entanto, alguns componentes COM exigem um modelo de Threading específico. A documentação do MSDN deve informá-lo quando esse for o caso.

> [!Note]  
> Na verdade, mesmo que você especifique o Threading Apartment, ainda é possível compartilhar interfaces entre threads, usando uma técnica chamada *marshaling*. O marshaling está além do escopo deste módulo. O ponto importante é que, com o Threading Apartment, você nunca deve simplesmente copiar um ponteiro de interface para outro thread. Para obter mais informações sobre os modelos de Threading COM, consulte [Processes, threads e Apartments](/windows/desktop/com/processes--threads--and-apartments).

 

Além dos sinalizadores já mencionados, é uma boa ideia definir o sinalizador de **\_ desabilitar \_ OLE1DDE do coinit** no parâmetro *dwCoInit* . A definição desse sinalizador evita alguma sobrecarga associada ao OLE (vinculação e inserção de objetos) 1,0, uma tecnologia obsoleta.

Veja como você deve inicializar COM para Threading Apartment:


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



O tipo de retorno **HRESULT** contém um erro ou código de êxito. Veremos o tratamento de erros COM na próxima seção.

## <a name="uninitializing-the-com-library"></a>Cancelando a inicialização da biblioteca COM

Para cada chamada bem-sucedida para [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), você deve chamar [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) antes de o thread sair. Essa função não usa parâmetros e não tem nenhum valor de retorno.


```C++
CoUninitialize();
```



## <a name="next"></a>Avançar

[Códigos de erro em COM](error-codes-in-com.md)

 

 