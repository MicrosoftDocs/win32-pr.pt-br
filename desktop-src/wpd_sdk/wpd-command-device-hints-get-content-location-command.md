---
description: O comando WPD COMMAND DEVICE HINTS GET CONTENT LOCATION recupera as \_ \_ \_ \_ \_ IDs de objeto de pastas que podem conter um objeto \_ de um tipo especificado.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (PortableDevice.h)
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
ms.openlocfilehash: 7e893df2a67aebcbd271d6df201e7e199b3c3326371e918b02b5c574ebba5763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026809"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>Comando WPD \_ DICAS DE DISPOSITIVO GET CONTENT \_ \_ \_ \_ \_ LOCATION

O **comando WPD \_ COMMAND DEVICE \_ \_ HINTS GET CONTENT \_ \_ \_ LOCATION** recupera as IDs de objeto de pastas que podem conter um objeto de um tipo especificado. Esse comando é fornecido como uma maneira mais rápida para um cliente descobrir onde um dispositivo armazena objetos específicos do que pela enumeração de objeto bruta.

## <a name="command-category"></a>Categoria de comando

**DICAS DE \_ DISPOSITIVO DE \_ CATEGORIA WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os parâmetros a seguir.



| Parâmetro                                   | VarType   | Descrição                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO DE CONTEÚDO \_ DE \_ DICAS DE \_ DISPOSITIVO \_ \_ DA PROPRIEDADE WPD | \_CLSID da VT | Obrigatórios. O tipo de objeto para o qual o chamador deseja encontrar o contêiner. Por exemplo, para encontrar as pastas de nível superior usadas para manter imagens em uma câmera digital, o chamador enviaria a IMAGEM DO TIPO \_ DE CONTEÚDO WPD. \_ \_ Consulte [Requisitos para objetos](requirements-for-objects.md) para uma lista de tipos de objeto definidos Windows Dispositivos Portáteis. |



 

## <a name="return-value"></a>Valor Retornado

O driver deve retornar os resultados a seguir.



| Resultado                                               | VarType     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **LOCAIS DE CONTEÚDO \_ DE DICAS DE DISPOSITIVO \_ \_ DE \_ \_ PROPRIEDADE WPD** | VT \_ UNKNOWN | Obrigatórios. Um [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) do tipo VT LPWSTR valores que especificam as IDs de objeto de pastas que contêm objetos do tipo indicado pelo parâmetro \_ de chamada. Se nenhuma pasta for encontrada, essa deverá ser uma lista vazia. As pastas indicadas pelo resultado podem ou não conter objetos de outros tipos de conteúdo. Consulte a [propriedade WPD \_ FOLDER CONTENT \_ TYPES \_ \_ ALLOWED](miscellaneous-properties.md) para obter informações sobre restrições de pasta.<br/> |
| **PROPRIEDADE WPD \_ \_ COMMON \_ HRESULT**                   | ERRO \_ DA VT   | Obrigatórios. Um **HRESULT** que indica êxito ou falha ao manipular o comando. Se o chamador estiver fazendo uma solicitação inválida, o driver deverá retornar **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** e não será necessário retornar nenhum outro valor de resultado. Os códigos de erro incluem Windows códigos de erro [dispositivos portáteis](error-constants.md) ou outros códigos de erro apropriados.                                                                                                                                                                            |
| **CÓDIGO DE ERRO DE \_ \_ DRIVER COMUM \_ \_ \_ DA PROPRIEDADE WPD**       | VT \_ UI4     | Opcional. Um código de erro específico do driver. Normalmente, isso é usado apenas para teste de driver ou se o driver, o dispositivo e o cliente são projetados juntos.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Chamando métodos

Só pode ser chamado diretamente usando [**IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 




