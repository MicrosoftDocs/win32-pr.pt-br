---
description: O \_ comando de ejeção de armazenamento de comando WPD \_ \_ ejeta um meio de armazenamento que pode ser ejetado remotamente pelo computador.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: WPD_COMMAND_STORAGE_EJECT comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a35b376ed9688217edfde03c76aed962d3e5fb74dc3d8bb7cc927ef1f621c9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839006"
---
# <a name="wpd_command_storage_eject-command"></a>Comando \_ de \_ ejeção de armazenamento de comando WPD \_

O comando de **\_ ejeção de \_ armazenamento \_ de comando WPD** ejeta um meio de armazenamento que pode ser ejetado remotamente pelo computador.

## <a name="command-category"></a>Categoria de comando

**\_armazenamento de categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                          | VarType    | Descrição                                             |
|------------------------------------|------------|---------------------------------------------------------|
| \_ID do \_ objeto de armazenamento de propriedade WPD \_ \_ | LPWStr do VT \_ | Obrigatórios. A ID de objeto do objeto de armazenamento a ser ejetado. |



 

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

 

 




