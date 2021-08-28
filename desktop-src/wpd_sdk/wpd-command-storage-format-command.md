---
description: O comando WPD \_ COMMAND \_ STORAGE FORMAT \_ formatará um objeto funcional de armazenamento no dispositivo.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: WPD_COMMAND_STORAGE_FORMAT Comando (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 353710bc4167b626b6af001ef535f6d21538a328609aaf05e5e8846415485914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806196"
---
# <a name="wpd_command_storage_format-command"></a>Comando WPD \_ COMMAND \_ STORAGE \_ FORMAT

O **comando WPD \_ COMMAND STORAGE \_ \_ FORMAT** formatará um objeto funcional de armazenamento no dispositivo.

## <a name="command-category"></a>Categoria de comando

**ARMAZENAMENTO DE \_ CATEGORIA \_ WPD**

## <a name="parameters"></a>Parâmetros

O driver espera os parâmetros a seguir.



| Parâmetro                          | VarType    | Descrição                                              |
|------------------------------------|------------|----------------------------------------------------------|
| ID DO \_ OBJETO DE ARMAZENAMENTO DE PROPRIEDADE \_ \_ \_ WPD | VT \_ LPWSTR | Obrigatórios. A ID do objeto da mídia de armazenamento a ser formatado. |



 

## <a name="return-value"></a>Valor Retornado

O driver deve retornar os resultados a seguir.



| Resultado                                         | VarType   | Descrição                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PROPRIEDADE WPD \_ \_ COMMON \_ HRESULT**             | ERRO \_ DA VT | Obrigatórios. Um **HRESULT** que indica êxito ou falha ao executar o comando. Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** e não será necessário retornar nenhum outro valor de resultado. Os códigos de erro incluem Windows de erro [dispositivos portáteis](error-constants.md) ou outros códigos de erro apropriados. |
| **CÓDIGO DE ERRO DE \_ \_ DRIVER COMUM \_ \_ \_ DA PROPRIEDADE WPD** | VT \_ UI4   | Opcional. Um código de erro específico do driver. Normalmente, isso é usado apenas para teste de driver ou se o driver, o dispositivo e o cliente são projetados juntos.                                                                                                                                                                                                                                |



 

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

 

 




