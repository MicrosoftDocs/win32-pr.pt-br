---
description: O \_ comando de formato de armazenamento de comando WPD \_ \_ formata um objeto funcional de armazenamento no dispositivo.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: WPD_COMMAND_STORAGE_FORMAT comando (PortableDevice. h)
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
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748678"
---
# <a name="wpd_command_storage_format-command"></a>\_Comando de \_ formato de armazenamento de comando WPD \_

O comando de **\_ formato de \_ armazenamento \_ de comando WPD** formata um objeto funcional de armazenamento no dispositivo.

## <a name="command-category"></a>Categoria de comando

**\_armazenamento de categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                          | VarType    | Descrição                                              |
|------------------------------------|------------|----------------------------------------------------------|
| \_ID do \_ objeto de armazenamento de propriedade WPD \_ \_ | LPWStr do VT \_ | Obrigatórios. A ID de objeto do meio de armazenamento a ser formatado. |



 

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

 

 




