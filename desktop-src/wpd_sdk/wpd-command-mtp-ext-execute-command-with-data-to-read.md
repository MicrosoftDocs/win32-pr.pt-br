---
description: O comando WPD COMMAND MTP EXT EXECUTE WITH DATA TO READ envia um bloco de comando \_ \_ \_ \_ \_ \_ \_ \_ MTP, que será \_ seguido por uma fase de dados. (Os dados são enviados do dispositivo para o host.).
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e5cfcb807978986c88406332e7270d3c21d5c59ae003c5f8a7fb1009d1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026755"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a>COMANDO WPD \_ \_ MTP \_ EXT EXECUTE COMMAND WITH DATA TO READ \_ \_ \_ \_ \_ \_ Command

O **comando WPD \_ COMMAND \_ MTP EXT EXECUTE \_ WITH DATA TO \_ \_ \_ \_ \_ \_ READ** envia um bloco de comando MTP, que será seguido por uma fase de dados. (Os dados são enviados do dispositivo para o host.)

## <a name="command-category"></a>Categoria de comando

**OPERAÇÕES DE FORNECEDOR EXT DA CATEGORIA WPD \_ \_ MTP \_ \_ \_**

## <a name="parameters"></a>Parâmetros

O driver espera os parâmetros a seguir.



| Parâmetro                                      | VarType | Descrição                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **CÓDIGO DE OPERAÇÃO EXT DA PROPRIEDADE WPD \_ \_ MTP \_ \_ \_**   | VT \_ UI4 | Obrigatórios. Identifica um código de operação MTP estendido pelo fornecedor.                                                                    |
| **PARAMS DE OPERAÇÃO EXT DA PROPRIEDADE WPD \_ \_ MTP \_ \_ \_** | VT \_ UI4 | Obrigatórios. Um **IPortableDevicePropVariantCollection**, que identifica os parâmetros necessários para o código de operação do fornecedor. |



 

## <a name="return-value"></a>Valor Retornado

O driver retorna os resultados a seguir.



| Resultado                                                       | VarType    | Descrição                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TAMANHO TOTAL DOS DADOS DE TRANSFERÊNCIA TOTAL DA PROPRIEDADE WPD \_ \_ MTP \_ EXT \_ \_ \_ \_**     | VT \_ UI8    | Obrigatórios. Retorna o tamanho total dos dados, em bytes, excluindo qualquer sobrecarga proveniente do dispositivo. Se o dispositivo relata dados desconhecidos (0xFFFFFFFF), o driver deve chamar **ReadData** repetidamente até que uma pequena parte seja recebida |
| **TAMANHO DO BUFFER DE TRANSFERÊNCIA IDEAL DA PROPRIEDADE WPD \_ \_ MTP \_ EXT \_ \_ \_ \_** | VT \_ UI4    | Opcional. Retorna o tamanho ideal do buffer de transferência.                                                                                                                                                                          |
| **CONTEXTO DE TRANSFERÊNCIA EXT \_ \_ DA PROPRIEDADE WPD MTP \_ \_ \_**               | VT \_ LPWSTR | Obrigatórios. Especifica o identificador de contexto para transferências de dados subsequentes.                                                                                                                                                           |



 

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

 

 




