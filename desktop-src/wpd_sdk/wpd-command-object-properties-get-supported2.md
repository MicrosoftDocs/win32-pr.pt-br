---
description: Recupera as propriedades com suporte por um objeto.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5020494658f380abc465a9059544131174edc8c417f69f6322636e6c9d4170d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703976"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>\_As propriedades do objeto de comando WPD \_ recebem o \_ \_ \_ comando com suporte

O **comando \_ \_ \_ \_ \_ com suporte das propriedades do objeto de comando WPD** recupera as propriedades com suporte de um objeto.

## <a name="command-category"></a>Categoria de comando

**\_Propriedades do \_ objeto de categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera o seguinte parâmetro.



| Parâmetro                                         | VarType        | Descrição                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **\_ID do \_ objeto de propriedades do objeto de propriedade WPD \_ \_ \_** | **LPWStr do VT \_** | Obrigatórios. A ID do objeto que contém as propriedades solicitadas. |



 

## <a name="return-value"></a>Valor Retornado

O driver deve retornar os seguintes resultados.



| Resultado                                                | VarType         | Descrição                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_chaves de \_ propriedade de propriedades do objeto de propriedade WPD \_ \_ \_** | **VT \_ desconhecido** | Obrigatórios. Uma interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que especifica todas as propriedades com suporte.                                                                                                                                                                                                            |
| **\_ \_ HRESULT comum de propriedade WPD \_**                    | **erro de VT \_**   | Obrigatórios. Um valor **HRESULT** que indica êxito ou falha geral. os possíveis valores de resultado incluem [Windows códigos de erro de dispositivos portáteis](error-constants.md). Se o chamador fizer uma solicitação inválida, o driver deverá retornar **HRESULT \_ do \_ Win32 ( \_ não \_ há suporte para o erro)** , mas, caso contrário, não será necessário retornar nenhum outro valor de resultado. |
| **\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**        | **\_UI4 VT**     | Opcional. Um código de erro específico do driver. Isso é normalmente usado apenas para testes de driver, ou se o driver, o dispositivo e o cliente estiverem todos criados juntos.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




