---
description: Controle de acesso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Controle de acesso (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837016"
---
# <a name="access-control-wpd-api"></a>Controle de acesso (API WPD)

O Windows Driver Model (WDM) dá suporte à restrição de acesso a dispositivos por meio de ACLs (listas de controle de acesso) nos nós de dispositivo de Plug and Play (PnP). Isso significa que os fornecedores e os administradores de rede podem restringir o acesso a qualquer tipo de dispositivo. Quando um aplicativo abre um identificador para um driver chamando [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), o Gerenciador de e/s do driver verifica se o usuário fornecido tem o acesso necessário e, da mesma forma, o Access verifica quando os IOCTLs são enviados para o driver a partir desse identificador.

Por exemplo, um administrador de rede pode restringir os usuários convidados a acesso somente leitura para dispositivos portáteis, enquanto eles poderiam conceder aos usuários autenticados acesso de leitura/gravação. Nesse caso, isso significa que, se um convidado emitisse um comando WPD que exigia acesso de leitura/gravação (como Delete Object); Ele falharia com acesso negado, enquanto que um usuário autenticado emitiu o mesmo comando, ele teria êxito.

As entradas de Política de Grupo para controlar o acesso ao armazenamento removível e aos dispositivos portáteis não são, na verdade, nada mais do que uma maneira fácil de os administradores aplicarem ACLs de nó de dispositivo PnP a uma classe inteira de dispositivos de cada vez (por exemplo, aplicar a permissão "negar acesso de gravação a dispositivos portáteis Política de Grupo" ajustaria as ACLs de todos os dispositivos WPD para negar acesso de gravação

## <a name="io-control-codes-in-wpd"></a>Códigos de controle de e/s em WPD

Aplicativos WPD se comunicam com drivers abrindo identificadores de dispositivo e enviando códigos de controle de e/s (IOCTLs). Esses IOCTLs consistem em quatro seções:

1.  Tipo de dispositivo
2.  Código de função
3.  Método de buffer
4.  Tipo de acesso

A quarta seção, o tipo de acesso, especifica o requisito de acesso específico para o comando fornecido. O Gerenciador de e/s do driver usa esses dados para executar a verificação da ACL (lista de controle de acesso).

Portanto, se um IOCTL foi definido como:


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



O Gerenciador de e/s do driver verificaria se o proprietário do identificador do dispositivo tem acesso de leitura ao dispositivo quando essa mensagem é enviada.

E, se um IOCTL foi definido como:


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



O Gerenciador de e/s do driver verificaria se o proprietário do identificador do dispositivo tem acesso de leitura/gravação ao dispositivo quando essa mensagem é enviada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do aplicativo**](application-overview.md)
</dt> <dt>

[**IPortableDevice:: abrir**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



