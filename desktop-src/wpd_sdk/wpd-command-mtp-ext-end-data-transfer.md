---
description: O comando \_ de \_ transferência de dados de extensão final MTP do comando WPD \_ \_ \_ \_ conclui uma transferência de dados e uma resposta de leitura do dispositivo.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812155"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>Comando \_ de \_ transferência de dados do MTP \_ ext \_ end \_ \_

O comando de **\_ transferência de \_ \_ dados de extensão \_ \_ \_ final MTP do comando WPD** conclui uma transferência de dados e uma resposta de leitura do dispositivo. A transferência é iniciada pelo comando [**WPD \_ de \_ \_ execução MTP \_ ext \_ \_ com \_ dados \_ para \_ ler**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) o comando ou o comando WPD de [**\_ \_ execução MTP \_ ext \_ \_ \_ com \_ dados \_ para \_ gravar**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) o comando.

## <a name="command-category"></a>Categoria de comando

**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                                      | VarType    | Descrição                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_** | LPWStr do VT \_ | Obrigatórios. Identifica o contexto que é retornado por uma chamada de método anterior. |



 

## <a name="return-value"></a>Valor Retornado

O driver retorna os seguintes resultados.



| Resultado                                        | VarType | Descrição                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_código de \_ resposta de MTP \_ ext da \_ Propriedade WPD \_**   | \_UI4 VT | Necessário. o código de resposta para o código de operação do fornecedor.                                                                                |
| **\_parâmetros de \_ resposta do MTP \_ ext de \_ Propriedade WPD \_** | \_UI4 VT | Opcional. Uma coleção **IPortableDevicePropVariantCollection** que identifica os parâmetros de resposta. Esta coleção pode estar vazia. |



 

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

 

