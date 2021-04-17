---
description: O comando \_ \_ obter dicas de dispositivo de comando para \_ \_ obter \_ local do conteúdo \_ recupera as IDs de objeto das pastas que podem conter um objeto de um tipo especificado.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782718"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>Comando de \_ dicas de dispositivo de comando WPD \_ \_ \_ obter \_ local do conteúdo \_

O **comando \_ obter dicas de dispositivo de comando para \_ \_ \_ obter \_ \_ local do conteúdo** recupera as IDs de objeto das pastas que podem conter um objeto de um tipo especificado. Esse comando é fornecido como uma maneira mais rápida para um cliente descobrir onde um dispositivo armazena objetos específicos do que pela enumeração de objeto bruta.

## <a name="command-category"></a>Categoria de comando

**\_dicas de \_ dispositivo de categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                                   | VarType   | Descrição                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo de \_ conteúdo de dicas de dispositivo de propriedade WPD \_ \_ \_ | CLSID do VT \_ | Obrigatórios. O tipo de objeto para o qual o chamador deseja localizar o contêiner. Por exemplo, para localizar as pastas de nível superior usadas para manter imagens em uma câmera digital, o chamador enviará uma \_ imagem de tipo de conteúdo WPD \_ \_ . Consulte [requisitos para objetos](requirements-for-objects.md) para obter uma lista de tipos de objetos definidos por dispositivos portáteis do Windows. |



 

## <a name="return-value"></a>Valor Retornado

O driver deve retornar os seguintes resultados.



| Resultado                                               | VarType     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_locais de \_ conteúdo de dicas de dispositivo de propriedade WPD \_ \_ \_** | VT \_ desconhecido | Obrigatórios. Um [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) dos valores de LPWStr do tipo VT \_ que especificam as IDs de objeto das pastas que contêm objetos do tipo indicado pelo parâmetro de chamada. Se nenhuma pasta for encontrada, ela deverá ser uma lista vazia. As pastas indicadas pelo resultado podem ou não conter objetos de outros tipos de conteúdo. Consulte a propriedade de [ \_ tipos de conteúdo de pasta WPD \_ \_ \_ permitida](miscellaneous-properties.md) para obter informações sobre restrições de pasta.<br/> |
| **\_ \_ HRESULT comum de propriedade WPD \_**                   | erro de VT \_   | Obrigatórios. Um **HRESULT** que indica êxito ou falha ao manipular o comando. Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 (erro \_ sem \_ suporte)** e não será necessário retornar nenhum outro valor de resultado. Os códigos de erro incluem [códigos de erro de dispositivos portáteis do Windows](error-constants.md) ou quaisquer outros códigos de erro apropriados.                                                                                                                                                                            |
| **\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**       | \_UI4 VT     | Opcional. Um código de erro específico do driver. Normalmente, isso é usado apenas para testes de driver, ou se o driver, o dispositivo e o cliente estiverem todos criados juntos.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Chamando métodos

Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

 




