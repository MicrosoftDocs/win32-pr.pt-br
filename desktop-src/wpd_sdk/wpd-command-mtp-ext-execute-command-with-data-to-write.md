---
description: O comando WPD de protocolo de \_ \_ \_ execução MTP ext \_ \_ \_ com \_ dados \_ para \_ gravar comando envia um bloco de comando MTP, seguido por uma fase de dados. Os dados são enviados do host para o dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791522"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>Comando \_ WPD \_ MTP \_ ext \_ comando \_ \_ com \_ dados \_ para \_ gravar comando

O comando WPD de protocolo de **\_ \_ \_ execução MTP ext \_ \_ \_ com \_ dados \_ para \_ gravar** comando envia um bloco de comando MTP, seguido por uma fase de dados. Os dados são enviados do host para o dispositivo.

## <a name="command-category"></a>Categoria de comando

**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                                                | VarType | Descrição                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_código de \_ operação do MTP \_ ext da \_ Propriedade WPD \_**             | \_UI4 VT | Obrigatórios. Identifica um código de operação MTP estendido pelo fornecedor.                                                                              |
| **\_parâmetros de \_ \_ operação de extensão MTP de propriedade \_ WPD \_**           | \_UI4 VT | Obrigatórios. Uma coleção **IPortableDevicePropVariantCollection** que identifica os parâmetros necessários para o código de operação do fornecedor. |
| **\_ \_ \_ \_ \_ Tamanho total dos \_ dados da transferência de extensão MTP \_ da propriedade WPD** | \_UI8 VT | Obrigatório. especifica o tamanho total dos dados, em bytes, excluindo qualquer sobrecarga, a ser enviada ao dispositivo.                                         |



 

## <a name="return-value"></a>Valor Retornado

O driver retorna os seguintes resultados.



| Resultado                                                       | VarType    | Descrição                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **\_tamanho do \_ \_ buffer de \_ \_ transferência ideal \_ de MTP ext \_ da propriedade WPD** | \_UI4 VT    | Obrigatórios. Especifica o tamanho ideal do buffer de transferência.                       |
| **\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**               | LPWStr do VT \_ | Opcional. Um identificador de contexto que o driver usa para transferências de dados subsequentes. |



 

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

 

 




