---
description: O comando \_ de \_ \_ dados de leitura ext do comando WPD \_ \_ recupera dados do dispositivo após o comando WPD do comando \_ \_ MTP \_ ext \_ Execute \_ \_ com \_ dados \_ para \_ ler o comando é executado.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: WPD_COMMAND_MTP_EXT_READ_DATA comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782717"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>Comando \_ de \_ dados de leitura do MTP ext de comandos \_ \_ WPD \_

O comando de **\_ \_ \_ \_ \_ dados de leitura ext do comando WPD** recupera dados do dispositivo após o comando WPD do comando **\_ \_ MTP \_ ext \_ Execute \_ \_ com \_ dados \_ para \_ ler** o comando é executado.

## <a name="command-category"></a>Categoria de comando

**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                                                   | VarType             | Descrição                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**              | LPWStr do VT \_          | Obrigatórios. Identifica o contexto que foi retornado pela chamada anterior ao dispositivo. |
| **\_a propriedade \_ WPD \_ \_ \_ \_ de bytes de transferência de extensão MTP \_ para \_ leitura** | \_UI4 VT             | Obrigatórios. Especifica o número de bytes a serem lidos.                                       |
| **\_dados de \_ transferência do MTP \_ ext da \_ Propriedade WPD \_**                 | \_UI1 de vetor \| VT \_ VT | Obrigatórios. Identifica o buffer no qual os dados do dispositivo são copiados.                  |



 

## <a name="return-value"></a>Valor Retornado

O driver retorna os seguintes resultados.



| Resultado                                                  | VarType             | Descrição                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **\_leitura de \_ bytes de transferência de extensão MTP da propriedade \_ \_ \_ WPD \_ \_** | \_UI4 VT             | Obrigatórios. Especifica o número de bytes recebidos do dispositivo. |
| **\_dados de \_ transferência do MTP \_ ext da \_ Propriedade WPD \_**             | \_UI1 de vetor \| VT \_ VT | Obrigatórios. O buffer que contém os dados do dispositivo.               |



 

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

 

 




