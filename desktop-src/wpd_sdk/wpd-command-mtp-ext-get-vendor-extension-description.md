---
description: O comando WPD de \_ \_ MTP \_ ext \_ Get de extensão de fornecedor da a linha \_ \_ \_ de comando recupera a cadeia de caracteres de descrição de extensão de fornecedor. Essa cadeia de caracteres é definida por um conjunto de DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793305"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>Comando \_ WPD \_ MTP \_ ext \_ \_ extensão Get Vendor \_ \_ Description

O comando **WPD de \_ \_ MTP \_ ext Get de \_ \_ extensão de fornecedor \_ \_** da a linha de comando recupera a cadeia de caracteres de descrição de extensão de fornecedor. Essa cadeia de caracteres é definida por um conjunto de **DeviceInfo** .

## <a name="command-category"></a>Categoria de comando

**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**

## <a name="parameters"></a>Parâmetros

Este comando não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

O driver retorna os seguintes resultados.



| Resultado                                                      | VarType    | Descrição                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **\_Descrição da \_ \_ extensão de \_ fornecedor MTP ext \_ \_ de propriedade WPD** | LPWStr do VT \_ | Obrigatórios. Especifica a cadeia de caracteres de descrição de extensão de fornecedor. |



 

## <a name="calling-methods"></a>Chamando métodos

Só pode ser chamado diretamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WpdMtpExtensions. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte a extensões de MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




