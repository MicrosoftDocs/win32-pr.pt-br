---
description: O comando WPD \_ COMMAND \_ MTP \_ EXT GET VENDOR EXTENSION DESCRIPTION recupera a cadeia de \_ \_ \_ \_ caracteres de descrição vendor-extension. Essa cadeia de caracteres é definida por um conjuntos de dados DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31622676161065ec685640789bc51eef64165542a9ebe4c9367ea1a03195e7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193500"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>Comando WPD \_ \_ MTP \_ EXT GET VENDOR EXTENSION \_ \_ \_ \_ DESCRIPTION

O **comando WPD \_ COMMAND \_ MTP EXT GET VENDOR \_ \_ EXTENSION \_ \_ \_ DESCRIPTION** recupera a cadeia de caracteres de descrição vendor-extension. Essa cadeia de caracteres é definida por um **conjuntos de dados DeviceInfo.**

## <a name="command-category"></a>Categoria de comando

**OPERAÇÕES DE FORNECEDOR EXT DA CATEGORIA WPD \_ \_ MTP \_ \_ \_**

## <a name="parameters"></a>Parâmetros

Esse comando não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

O driver retorna os resultados a seguir.



| Resultado                                                      | VarType    | Descrição                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **DESCRIÇÃO DA EXTENSÃO DE FORNECEDOR EXT DA PROPRIEDADE WPD \_ \_ MTP \_ \_ \_ \_** | VT \_ LPWSTR | Obrigatórios. Especifica a cadeia de caracteres de descrição da extensão de fornecedor. |



 

## <a name="calling-methods"></a>Chamando métodos

Só pode ser chamado diretamente usando [**IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte a extensões MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




