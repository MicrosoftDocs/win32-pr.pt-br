---
title: Códigos de erro do dispositivo
description: Os métodos InvokeAction e QueryStateVariable retornam valores HRESULT que podem indicar um erro de dispositivo (ou seja, um erro que é recebido de um dispositivo certificado pelo UPnP).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104454421"
---
# <a name="device-error-codes"></a>Códigos de erro do dispositivo

Os métodos [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) retornam valores **HRESULT** que podem indicar um erro de dispositivo (ou seja, um erro que é recebido de um dispositivo certificado pelo UPnP). Se um erro for recebido de um dispositivo, o método ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) ou [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) retornará um valor **HRESULT** com base no código de erro do dispositivo, conforme explicado neste tópico. Como uma conversão é aplicada ao código de erro do dispositivo para produzir um valor **HRESULT** , você não pode ler o código de erro do dispositivo diretamente do valor **HRESULT** .

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a>Conversão de um código de erro de dispositivo para um HRESULT

Há códigos de erro padrão e não padrão do dispositivo. Os códigos padrão têm o mesmo significado em todos os dispositivos certificados pelo UPnP e têm valores inferiores a 600. Os códigos não padrão são específicos do fornecedor e têm valores variados de 600 a 899.

Se o código de erro do dispositivo é ou não padrão determina como o valor **HRESULT** é gerado:

-   Um código de erro de dispositivo padrão é mapeado para um valor **HRESULT** .

<!-- -->

-   Um código de erro de dispositivo não padrão é inserido no valor **HRESULT** aplicando uma fórmula.

Esses dois procedimentos podem ser revertidos para determinar o código de erro do dispositivo a partir de um valor **HRESULT** específico.

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a>Derivando um código de erro de dispositivo de um valor HRESULT

Se o valor **HRESULT** for maior ou igual a um **UPnP e a \_ \_ \_ \_ base específica da ação** (0x80040300) e menor ou igual a **UPnP e a \_ \_ ação \_ específica \_ Max** (0x8004042B), o código de erro do dispositivo não será padrão — Use a fórmula na seção a seguir para determinar o código de erro. Caso contrário, o código de erro do dispositivo é padrão: Use a tabela na seção mapeamento para códigos de erro de dispositivo padrão, que fornece o mapeamento do valor **HRESULT** para o código de erro do dispositivo.

Para obter uma descrição de texto do erro após uma chamada para [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), defina o parâmetro *pvarRetVal* como uma matriz vazia. No retorno, esse parâmetro conterá uma descrição de texto do erro, caso tenha ocorrido.

### <a name="formula-for-nonstandard-device-error-codes"></a>Fórmula para códigos de erro não padrão do dispositivo

Use a fórmula a seguir se a **ação de UPnP \_ e a \_ \_ \_ base especificarem** a partir de uma ação de UPnP e a **\_ \_ Action \_ \_** específicas 

Código de erro do dispositivo = (**HRESULT**  -  **UPnP \_ E a \_ \_ \_ base específica da ação**) + **\_ \_ \_ base específica da ação de falha**

Substituindo os valores numéricos reais, a equação é: código de erro do dispositivo = (**HRESULT** -0x80040300) + 0x0258

### <a name="mapping-for-standard-device-error-codes"></a>Mapeamento para códigos de erro de dispositivo padrão

Use o mapeamento a seguir se a  <  **\_ \_ \_ \_ base específica de ação E UPnP** do HRESULT.



| Valor HRESULT                    | Código de erro do dispositivo                | Valor real |
|----------------------------------|----------------------------------|--------------|
| \_ \_ ação inválida E UPnP \_         | \_ação inválida de falha \_           | 401          |
| \_argumentos UPnP E \_ inválidos \_      | ARG. de falha \_ inválido \_              | 402          |
| UPNP \_ E \_ fora \_ de \_ sincronização           | \_número de \_ sequência \_ inválido de falha | 403          |
| \_variável UPnP E \_ inválida \_       | \_variável inválida de falha \_         | 404          |
| \_ \_ \_ falha na solicitação de ação E UPnP \_ | \_ \_ erro interno do dispositivo de falha \_   | 501          |



 

## <a name="more-information"></a>Mais informações

Os códigos de erro do dispositivo são especificados na [arquitetura de dispositivo UPnP versão 1,0](https://openconnectivity.org/resources/documents.asp). As constantes mencionadas neste tópico são definidas nos arquivos UPnP. h e UPnP. idl.

 

 




