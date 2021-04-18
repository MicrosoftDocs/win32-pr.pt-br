---
description: O comando \_ WPD \_ ainda \_ o \_ \_ comando Iniciar captura de imagem inicia uma captura de imagem ainda por um objeto funcional de imagem ainda. Se um novo objeto for criado como resultado de tirar uma foto, o driver deverá enviar o evento de \_ evento \_ adicionado do WPD \_ .
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE comando (PortableDevice. h)
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
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796279"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>Comando \_ WPD \_ ainda \_ \_ \_ comando Iniciar captura de imagem

O comando **WPD ainda o comando \_ \_ \_ \_ \_ Iniciar captura de imagem** inicia uma captura de imagem ainda por um objeto funcional de imagem ainda. Se um novo objeto for criado como resultado de tirar uma foto, o driver deverá enviar o evento **de \_ evento \_ \_ adicionado do WPD** .

## <a name="command-category"></a>Categoria de comando

**a \_ categoria \_ WPD \_ ainda \_ captura de imagem**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                              | VarType    | Descrição                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_destino de \_ \_ comando comum de propriedade \_ WPD | LPWStr do VT \_ | Obrigatórios. A ID de objeto do objeto funcional de captura de imagem ainda no dispositivo que deve assumir a imagem. Cada objeto funcional de captura de imagem ainda pode ter configurações diferentes e pode se referir a um hardware diferente em um dispositivo (por exemplo, uma câmera frontal ou traseira de um telefone) e esse parâmetro indica qual deles usar.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O driver deve retornar os seguintes resultados.



| Resultado                                         | VarType   | Descrição                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ HRESULT comum de propriedade WPD \_**             | erro de VT \_ | Obrigatórios. Um **HRESULT** que indica êxito ou falha ao executar o comando. Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado. Os códigos de erro incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md) ou quaisquer outros códigos de erro apropriados. |
| **\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_** | \_UI4 VT   | Opcional. Um código de erro específico do driver. Esse valor normalmente é usado por fornecedores de dispositivo para melhorar o diagnóstico de erros de dispositivo ao usar seus aplicativos. Os aplicativos de uso geral podem ignorá-lo e confiar exclusivamente na \_ Propriedade WPD \_ comum \_ HRESULT.                                                                                                                   |



 

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

 

 




