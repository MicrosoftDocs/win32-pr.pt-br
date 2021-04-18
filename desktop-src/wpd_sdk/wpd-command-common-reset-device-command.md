---
description: O comando \_ do \_ dispositivo de redefinição comum de comandos WPD \_ \_ redefine o dispositivo. Isso não significa reformatação; é equivalente a desligar e ligar o dispositivo novamente.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: WPD_COMMAND_COMMON_RESET_DEVICE comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760675"
---
# <a name="wpd_command_common_reset_device-command"></a>Comando \_ de \_ \_ dispositivo de redefinição comum de comandos WPD \_

O comando do **\_ \_ \_ \_ dispositivo de redefinição comum de comandos WPD** redefine o dispositivo. Isso não significa reformatação; é equivalente a desligar e ligar o dispositivo novamente.

## <a name="command-category"></a>Categoria de comando

**Categoria de WPD \_ \_ comum**

## <a name="parameters"></a>Parâmetros

Este comando não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

O driver deve retornar os seguintes resultados.



| Resultado                                         | VarType   | Descrição                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ HRESULT comum de propriedade WPD \_**             | erro de VT \_ | Obrigatórios. Um **HRESULT** que indica êxito ou falha ao executar o comando. Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado. Os códigos de erro incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md) ou quaisquer outros códigos de erro apropriados. |
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

 

 




