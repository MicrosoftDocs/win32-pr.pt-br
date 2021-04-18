---
description: O comando do WPD de \_ \_ MTP \_ ext Command \_ \_ \_ com \_ dados \_ para \_ ler comando envia um bloco de comando MTP, que será seguido por uma fase de dados. (Os dados são enviados do dispositivo para o host.).
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807879"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a>Comando \_ WPD \_ \_ de MTP ext Command \_ \_ \_ com \_ dados \_ para \_ ler comando

O comando do **WPD de \_ \_ MTP \_ ext Command \_ \_ \_ com \_ dados \_ para \_ ler** comando envia um bloco de comando MTP, que será seguido por uma fase de dados. (Os dados são enviados do dispositivo para o host.)

## <a name="command-category"></a>Categoria de comando

**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                                      | VarType | Descrição                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **\_código de \_ operação do MTP \_ ext da \_ Propriedade WPD \_**   | \_UI4 VT | Obrigatórios. Identifica um código de operação MTP estendido pelo fornecedor.                                                                    |
| **\_parâmetros de \_ \_ operação de extensão MTP de propriedade \_ WPD \_** | \_UI4 VT | Obrigatórios. Um **IPortableDevicePropVariantCollection**, que identifica os parâmetros necessários para o código de operação do fornecedor. |



 

## <a name="return-value"></a>Valor Retornado

O driver retorna os seguintes resultados.



| Resultado                                                       | VarType    | Descrição                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ \_ Tamanho total dos \_ dados da transferência de extensão MTP \_ da propriedade WPD**     | \_UI8 VT    | Obrigatórios. Retorna o tamanho total dos dados, em bytes, excluindo qualquer sobrecarga proveniente do dispositivo. Se o dispositivo relatar um DataSize desconhecido (0xFFFFFFFF), o driver deverá chamar **ReadData** repetidamente até que um pequeno bloco seja recebido |
| **\_tamanho do \_ \_ buffer de \_ \_ transferência ideal \_ de MTP ext \_ da propriedade WPD** | \_UI4 VT    | Opcional. Retorna o tamanho ideal do buffer de transferência.                                                                                                                                                                          |
| **\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**               | LPWStr do VT \_ | Obrigatórios. Especifica o identificador de contexto para transferências de dados subsequentes.                                                                                                                                                           |



 

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

 

 




