---
description: O comando de \_ dados de gravação de extensão MTP do comando WPD \_ \_ \_ \_ envia dados para o dispositivo depois que o comando do WPD do comando \_ \_ MTP ext de \_ \_ execução \_ \_ com \_ dados \_ para \_ gravar é executado.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: WPD_COMMAND_MTP_EXT_WRITE_DATA comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789339"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a>Comando \_ de \_ dados de gravação do MTP ext do comando \_ \_ WPD \_

O comando de **\_ dados de \_ \_ \_ gravação \_ de extensão MTP do comando WPD** envia dados para o dispositivo depois que o comando do WPD do comando **\_ \_ MTP ext de \_ \_ execução \_ \_ com \_ dados \_ para \_ gravar** é executado.

## <a name="command-category"></a>Categoria de comando

**\_operações do \_ fornecedor de MTP \_ ext da \_ categoria WPD \_**

## <a name="parameters"></a>Parâmetros

O driver espera os seguintes parâmetros.



| Parâmetro                                                    | VarType             | Descrição                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **\_contexto de \_ \_ transferência de extensão MTP da propriedade \_ WPD \_**               | LPWStr do VT \_          | Obrigatórios. Identifica o contexto que foi retornado pela chamada anterior ao dispositivo. |
| **\_a propriedade \_ WPD \_ de transferência de extensão MTP \_ \_ \_ \_ de criação de bytes para \_ gravação** | \_UI4 VT             | Obrigatórios. Especifica o número de bytes a serem gravados.                                      |
| **\_dados de \_ transferência do MTP \_ ext da \_ Propriedade WPD \_**                  | \_UI1 de vetor \| VT \_ VT | Obrigatórios. Identifica o buffer no qual os dados do dispositivo são copiados.                  |



 

## <a name="return-value"></a>Valor Retornado

O driver retorna os seguintes resultados.



| Resultado                                                     | VarType | Descrição                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| **\_bytes de \_ número de transferência de extensão MTP da propriedade WPD \_ \_ \_ \_ \_ gravados** | \_UI4 VT | Obrigatórios. Especifica o número de bytes enviados ao dispositivo. |



 

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

 

 




