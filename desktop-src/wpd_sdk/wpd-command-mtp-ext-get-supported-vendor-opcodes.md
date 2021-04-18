---
description: O comando \_ WPD \_ ext de provedor de \_ código de operação de \_ Get \_ com suporte \_ \_ do Não há nenhuma fase de dados subsequente associada a este comando.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763064"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>Comando WPD de \_ \_ MTP \_ ext de \_ \_ fornecedor com suporte \_ \_

O comando **WPD \_ ext de provedor de código de \_ \_ \_ \_ \_ \_ operação de Get com suporte** do Não há nenhuma fase de dados subsequente associada a este comando.

## <a name="command-category"></a>Categoria de comando

**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**

## <a name="parameters"></a>Parâmetros

Este comando não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

O driver retorna os seguintes resultados.



| Resultado                                                | VarType | Descrição                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **\_códigos de \_ operação de fornecedor de MTP \_ ext de \_ \_ Propriedade WPD \_** | \_UI4 VT | Obrigatórios. Um **IPortableDevicePropVariantCollection** que contém todos os códigos de operação estendidos pelo fornecedor. |



 

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

 

 




