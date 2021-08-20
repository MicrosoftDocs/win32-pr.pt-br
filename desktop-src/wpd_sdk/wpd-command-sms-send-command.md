---
description: O comando \_ de \_ envio de SMS do comando WPD \_ inicia o envio de uma mensagem SMS (Short Message Service) por um objeto funcional do SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: WPD_COMMAND_SMS_SEND comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: cd68d064614dde3e4e20fed75841ef88f51fc2ad2ed5b43af33398ec636b5ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026488"
---
# <a name="wpd_command_sms_send-command"></a>Comando \_ de \_ envio de SMS de comandos WPD \_

O comando de **\_ envio de \_ SMS \_ do comando WPD** inicia o envio de uma mensagem SMS (Short Message Service) por um objeto funcional do SMS.

## <a name="command-category"></a>Categoria de comando

**Categoria de WPD do \_ \_ SMS**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                              | VarType             | Descrição                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_destino de \_ \_ comando comum de propriedade \_ WPD | LPWStr do VT \_          | Obrigatórios. A ID de objeto do objeto funcional do SMS que deve enviar a mensagem. Diferentes objetos funcionais do SMS podem ter configurações diferentes.                                                                                     |
| \_destinatário de \_ SMS da propriedade WPD \_          | LPWStr do VT \_          | Obrigatórios. O URI do destinatário.                                                                                                                                                                                                  |
| \_tipo de \_ \_ mensagem SMS da propriedade \_ WPD      | \_UI4 VT             | Obrigatórios. Um enumerador de [**\_ \_ tipos de mensagem SMS**](sms-message-types.md) que indica o tipo de mensagem (texto ou binário).                                                                                                        |
| \_mensagem de \_ \_ texto SMS da propriedade \_ WPD      | LPWStr do VT \_          | Opcional. Se **o \_ \_ tipo de \_ mensagem \_ de SMS de propriedade WPD** indicar uma mensagem de texto, essa será a cadeia de caracteres de mensagem; caso contrário, esse parâmetro não será incluído.                                                                                  |
| \_mensagem de \_ binário de SMS de propriedade WPD \_ \_    | \_UI1 de vetor \| VT \_ VT | Opcional. Se **o \_ \_ tipo de \_ mensagem \_ de SMS de propriedade WPD** indicar uma mensagem binária, esse será um ponteiro para uma matriz de bytes; caso contrário, esse parâmetro não será incluído. A primeira DWORD do valor é o comprimento da matriz, em bytes. |



 

## <a name="return-value"></a>Valor Retornado

O driver deve retornar os seguintes resultados.



| Resultado                                         | VarType   | Descrição                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ HRESULT comum de propriedade WPD \_**             | erro de VT \_ | Obrigatórios. Um **HRESULT** que indica êxito ou falha ao executar o comando. Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado. os códigos de erro incluem [Windows códigos de erro de dispositivos portáteis](error-constants.md) ou quaisquer outros códigos de erro apropriados. |
| **\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_** | \_UI4 VT   | Opcional. Um código de erro específico do driver. Normalmente, isso é usado apenas para testes de driver, ou se o driver, o dispositivo e o cliente estiverem todos criados juntos.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Chamando métodos

Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




