---
description: O comando WPD \_ COMMAND STILL IMAGE CAPTURE INITIATE inicia uma captura de imagem ainda por um objeto funcional de \_ imagem \_ \_ \_ ainda. Se um novo objeto for criado como resultado de tirar uma foto, o driver deverá enviar o evento WPD \_ EVENT \_ OBJECT \_ ADDED.
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE Comando (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5c5490a5af583753f504decacaccf4b4373890fdb7f0e5b099389df29cdc0571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806276"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>Comando WPD \_ AINDA CAPTURA DE IMAGEM COMANDO \_ \_ \_ \_ INITIATE

O **comando WPD \_ COMMAND STILL IMAGE CAPTURE \_ \_ \_ \_ INITIATE** inicia uma captura de imagem ainda por um objeto funcional de imagem ainda. Se um novo objeto for criado como resultado de tirar uma foto, o driver deverá enviar o **evento WPD \_ EVENT OBJECT \_ \_ ADDED.**

## <a name="command-category"></a>Categoria de comando

**CAPTURA DE IMAGEM \_ AINDA \_ DA CATEGORIA \_ \_ WPD**

## <a name="parameters"></a>Parâmetros

O driver espera os parâmetros a seguir.



| Parâmetro                              | VarType    | Descrição                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DESTINO DE COMANDO \_ COMUM DA \_ PROPRIEDADE \_ WPD \_ | VT \_ LPWSTR | Obrigatórios. A ID do objeto funcional de captura de imagem ainda no dispositivo que deve tirar a imagem. Cada objeto funcional de captura de imagem ainda pode ter configurações diferentes e pode se referir a um hardware diferente em um dispositivo (por exemplo, uma câmera frontal ou traseira de um telefone) e esse parâmetro indica qual delas usar.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O driver deve retornar os resultados a seguir.



| Resultado                                         | VarType   | Descrição                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PROPRIEDADE WPD \_ \_ COMMON \_ HRESULT**             | ERRO \_ DA VT | Obrigatórios. Um **HRESULT** que indica êxito ou falha ao executar o comando. Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** e não será necessário retornar nenhum outro valor de resultado. Os códigos de erro incluem Windows de erro [dispositivos portáteis](error-constants.md) ou outros códigos de erro apropriados. |
| **CÓDIGO DE ERRO DE \_ \_ DRIVER COMUM \_ \_ \_ DA PROPRIEDADE WPD** | VT \_ UI4   | Opcional. Um código de erro específico do driver. Normalmente, esse valor é usado por fornecedores de dispositivos para melhorar o diagnóstico de erros de dispositivo ao usar seus aplicativos. Em vez disso, os aplicativos de uso geral o ignorariam e confiariam exclusivamente na \_ \_ PROPRIEDADE WPD COMMON \_ HRESULT.                                                                                                                   |



 

## <a name="calling-methods"></a>Chamando métodos

Só pode ser chamado diretamente usando [**IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




