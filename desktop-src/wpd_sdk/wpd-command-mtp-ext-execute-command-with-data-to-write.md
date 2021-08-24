---
description: O comando WPD COMMAND MTP EXT EXECUTE WITH DATA TO WRITE envia um bloco de comando \_ \_ \_ \_ \_ \_ \_ \_ MTP, que é \_ seguido por uma fase de dados. Os dados são enviados do host para o dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae0e50ad2fad9967252d9a21c1e864d056338a3e3a2b82f4c29d951a722953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806306"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>COMANDO WPD \_ \_ MTP \_ EXT EXECUTE COMMAND WITH DATA TO WRITE \_ \_ \_ \_ \_ \_ Command

O **comando WPD \_ COMMAND \_ MTP EXT EXECUTE \_ WITH DATA TO \_ \_ \_ \_ \_ \_ WRITE** envia um bloco de comando MTP, que é seguido por uma fase de dados. Os dados são enviados do host para o dispositivo.

## <a name="command-category"></a>Categoria de comando

**OPERAÇÕES DE FORNECEDOR EXT DA CATEGORIA WPD \_ \_ MTP \_ \_ \_**

## <a name="parameters"></a>Parâmetros

O driver espera os parâmetros a seguir.



| Parâmetro                                                | VarType | Descrição                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **CÓDIGO DE OPERAÇÃO EXT DA PROPRIEDADE WPD \_ \_ MTP \_ \_ \_**             | VT \_ UI4 | Obrigatórios. Identifica um código de operação MTP estendido pelo fornecedor.                                                                              |
| **PARAMS DE OPERAÇÃO EXT DA PROPRIEDADE WPD \_ \_ MTP \_ \_ \_**           | VT \_ UI4 | Obrigatórios. Uma **coleção IPortableDevicePropVariantCollection** que identifica os parâmetros necessários para o código de operação do fornecedor. |
| **TAMANHO TOTAL DOS DADOS DE TRANSFERÊNCIA TOTAL DA PROPRIEDADE WPD \_ \_ MTP \_ EXT \_ \_ \_ \_** | VT \_ UI8 | Required.Especifica o tamanho total dos dados, em bytes, excluindo qualquer sobrecarga, a ser enviado ao dispositivo.                                         |



 

## <a name="return-value"></a>Valor Retornado

O driver retorna os resultados a seguir.



| Resultado                                                       | VarType    | Descrição                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **TAMANHO DO BUFFER DE TRANSFERÊNCIA IDEAL DA PROPRIEDADE WPD \_ \_ MTP \_ EXT \_ \_ \_ \_** | VT \_ UI4    | Obrigatórios. Especifica o tamanho ideal do buffer de transferência.                       |
| **CONTEXTO DE TRANSFERÊNCIA EXT \_ \_ DA PROPRIEDADE WPD MTP \_ \_ \_**               | VT \_ LPWSTR | Opcional. Um identificador de contexto que o driver usa para transferências de dados subsequentes. |



 

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

 

 




