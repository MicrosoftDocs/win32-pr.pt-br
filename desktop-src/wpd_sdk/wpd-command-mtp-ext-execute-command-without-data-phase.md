---
description: O comando WPD de \_ \_ MTP \_ ext Command \_ \_ \_ sem \_ \_ comando de fase de dados envia um bloco de comando MTP. Não há nenhuma fase de dados subsequente associada a este comando.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE comando (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c4d1d5af4d1e4e712f3a39dd5cbb296133bb16f4de3b677da4a45fa7bbc204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806296"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>Comando \_ WPD \_ MTP \_ ext \_ comando de execução \_ \_ sem \_ Data \_ Phase comando

O comando **WPD de \_ \_ MTP ext Command \_ \_ \_ \_ sem \_ \_** comando de fase de dados envia um bloco de comando MTP. Não há nenhuma fase de dados subsequente associada a este comando.

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



| Resultado                                        | VarType | Descrição                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **\_código de \_ resposta de MTP \_ ext da \_ Propriedade WPD \_**   | \_UI4 VT | Obrigatórios. O código de resposta para o código de operação do fornecedor.                                                                      |
| **\_parâmetros de \_ resposta do MTP \_ ext de \_ Propriedade WPD \_** | \_UI4 VT | Opcional. Um **IPortableDevicePropVariantCollection** que identifica os parâmetros de resposta. Esta coleção pode estar vazia. |



 

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

 

 




