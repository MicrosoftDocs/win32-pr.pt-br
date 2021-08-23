---
description: Controle de acesso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Controle de acesso (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83caa01b08409afd196ea0507cb47986928a1d947b6ff7907640e4f9bd5b390f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657906"
---
# <a name="access-control-wpd-api"></a>Controle de acesso (API WPD)

O WDM (Windows Driver Model) do Windows dá suporte à restrição do acesso ao dispositivo por meio de ACLs (listas de controle de acesso) nos nós de dispositivo Plug and Play (PnP). Isso significa que os fornecedores e administradores de rede podem restringir o acesso a qualquer tipo de dispositivo. Quando um aplicativo abre um handle para um driver chamando [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), o Gerenciador de E/S do driver verifica se o usuário determinado tem o acesso necessário e, da mesma forma, faz verificações de acesso quando IOCTLs são enviadas para o driver desse manipular.

Por exemplo, um administrador de rede pode restringir os usuários convidados ao acesso somente leitura para dispositivos portáteis, enquanto eles podem conceder aos usuários autenticados acesso de leitura/gravação. Nesse caso, isso implica que, se um convidado emitiu um comando WPD que exigia acesso de leitura/gravação (como Excluir Objeto); ele falharia com Acesso Negado, enquanto se um usuário autenticado tivesse emitido o mesmo comando, teria êxito.

As entradas Política de Grupo para controlar o acesso ao armazenamento removível e a dispositivos portáteis não são nada mais do que uma maneira fácil para os administradores aplicarem ACLs de nó de dispositivo PnP a uma classe inteira de dispositivos por vez (por exemplo, aplicar o Política de Grupo "Negar acesso de gravação a dispositivos portáteis" ajustaria as ACLs de todos os dispositivos WPD para negar o acesso de gravação).

## <a name="io-control-codes-in-wpd"></a>Códigos de controle de E/S no WPD

Os aplicativos WPD se comunicam com drivers abrindo os controles de dispositivo e enviando IOCTLs (códigos de controle de E/S). Essas IOCTLs consistem em quatro seções:

1.  Tipo de dispositivo
2.  Código de função
3.  Método Buffer
4.  Tipo de acesso

A quarta seção, o Tipo de Acesso, especifica o requisito de acesso específico para o comando especificado. O gerenciador de E/S do driver usa esses dados para executar a verificação de ACL (Lista de Controle de Acesso).

Portanto, se um IOCTL tiver sido definido como:


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



O gerenciador de E/S do driver verificaria se o proprietário da alça do dispositivo tem acesso de leitura ao dispositivo quando essa mensagem é enviada.

E, se um IOCTL fosse definido como:


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



O gerenciador de E/S do driver verificaria se o proprietário do dispositivo tem acesso de leitura/gravação ao dispositivo quando essa mensagem é enviada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do aplicativo**](application-overview.md)
</dt> <dt>

[**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



