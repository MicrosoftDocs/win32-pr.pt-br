---
title: Propriedade IsBeating de IVMGuestOS (VPCCOMInterfaces.h)
description: Determina se a máquina virtual tem uma pulsação.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Propriedade IsBeatbeating Pc Virtual
- Propriedade IsBeatbeating Pc Virtual , interface IVMGuestOS
- INTERFACE IVMGuestOS Pc Virtual , propriedade IsBeatbeating
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91598284d3765c5ff6de185ca0cf3b652036c226d80b0fe01a9944a9d7480b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594176"
---
# <a name="ivmguestosisheartbeating-property"></a>Propriedade IVMGuestOS::IsBeatbeating

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se a máquina virtual tem uma pulsação.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Valor da propriedade

**VARIANT \_ TRUE** se uma pulsação for detectada; **caso \_ contrário, VARIANT FALSE.**

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                              | Significado                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | A operação foi bem-sucedida.<br/>                                                                                                                         |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                   | O parâmetro é **NULL.**<br/>                                                                                                                            |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | A configuração é desconhecida.<br/>                                                                                                                         |
| <dl> <dt>VM \_ E \_ VM \_ NÃO \_ EXECUTANDO</dt> <dt>0XA0040206</dt> </dl>      | A máquina virtual deve estar em execução para essa operação.<br/>                                                                                               |
| <dl> <dt>VM \_ E \_ ADIÇÕES \_ NÃO SÃO \_ 0XA0040504</dt> <dt></dt> </dl> | A máquina virtual não está totalmente inicializada, o recurso de componentes de integração não está instalado ou a versão instalada não dá suporte a esse recurso.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Ocorreu um erro inesperado.<br/>                                                                                                                     |



## <a name="remarks"></a>Comentários

Quando os componentes de integração são instalados no sistema operacional convidado, um 'tique' ou pulsação regular é enviado da sessão da máquina virtual para Windows Virtual PC. Se o sistema operacional convidado estiver muito carregado, é possível que o COMPUTADOR Virtual receba menos pulsações do que o esperado. Se nenhuma pulsação for detectada, é possível que o sistema operacional convidado não está respondendo ou está com problemas.

Por padrão, uma máquina virtual produz dez tiques de pulsação por minuto. Se nenhum tique de pulsação for detectado por um minuto inteiro, o Windows Virtual PC tentará reiniciar a sessão da máquina virtual uma vez a cada dez segundos por até dois minutos. Esse comportamento é controlado pelos seguintes valores de chave no arquivo de configuração da sessão da máquina virtual.



| Chave de configuração                                            | Padrão       | Descrição                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| integration/microsoft/heartbeat/time<br/>              | 60<br/> | O comprimento do bloco de tempo usado para gerar tiques de pulsação, em segundos.<br/>                                             |
| integration/microsoft/heartbeat/rate<br/>              | 10<br/> | O número de tiques gerados em cada bloco de tempo de pulsação.<br/>                                                                  |
| integration/microsoft/heartbeat/failure \_ interval<br/> | 10<br/> | O número de segundos entre as tentativas de reinicialização, uma vez que nenhum tique de pulsação é recebido dentro de um bloco de tempo de pulsação específico.<br/> |
| tentativas de integração/microsoft/pulsação/falha \_<br/> | 12<br/> | O número de tentativas de reinicialização feitas.<br/>                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

