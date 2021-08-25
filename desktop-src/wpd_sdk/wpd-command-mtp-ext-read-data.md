---
description: O comando WPD COMMAND MTP EXT READ DATA recupera dados do dispositivo depois que o comando \_ \_ \_ \_ \_ WPD \_ COMMAND \_ MTP \_ EXT EXECUTE WITH DATA TO READ é \_ \_ \_ \_ \_ \_ executado.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: WPD_COMMAND_MTP_EXT_READ_DATA comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5aeee37e1922f91e9a9fac7881369364d01340893829678a5651f89ed428440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927946"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>Comando WPD \_ \_ MTP \_ EXT READ \_ \_ DATA

O **comando WPD \_ COMMAND \_ MTP EXT READ \_ \_ \_ DATA** recupera dados do dispositivo depois que o comando **WPD COMMAND \_ \_ MTP EXT EXECUTE \_ WITH DATA TO \_ \_ \_ \_ \_ \_ READ** é executado.

## <a name="command-category"></a>Categoria de comando

**OPERAÇÕES DE FORNECEDOR EXT DA CATEGORIA WPD \_ \_ MTP \_ \_ \_**

## <a name="parameters"></a>Parâmetros

O driver espera os parâmetros a seguir.



| Parâmetro                                                   | VarType             | Descrição                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **CONTEXTO DE TRANSFERÊNCIA EXT \_ \_ DA PROPRIEDADE WPD MTP \_ \_ \_**              | VT \_ LPWSTR          | Obrigatórios. Identifica o contexto retornado pela chamada anterior ao dispositivo. |
| **PROPRIEDADE WPD \_ \_ MTP \_ EXT TRANSFER NUM BYTES TO \_ \_ \_ \_ \_ READ** | VT \_ UI4             | Obrigatórios. Especifica o número de bytes a ler.                                       |
| **DADOS DE TRANSFERÊNCIA EXT DA PROPRIEDADE WPD \_ \_ MTP \_ \_ \_**                 | VT \_ VECTOR \| VT \_ UI1 | Obrigatórios. Identifica o buffer no qual os dados do dispositivo são copiados.                  |



 

## <a name="return-value"></a>Valor Retornado

O driver retorna os resultados a seguir.



| Resultado                                                  | VarType             | Descrição                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **PROPRIEDADE WPD \_ \_ MTP \_ EXT TRANSFER NUM BYTES \_ \_ \_ \_ READ** | VT \_ UI4             | Obrigatórios. Especifica o número de bytes recebidos do dispositivo. |
| **DADOS DE TRANSFERÊNCIA EXT DA PROPRIEDADE WPD \_ \_ MTP \_ \_ \_**             | VT \_ VECTOR \| VT \_ UI1 | Obrigatórios. O buffer que contém os dados do dispositivo.               |



 

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

 

 




