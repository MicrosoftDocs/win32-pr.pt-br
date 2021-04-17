---
title: Propriedade ispulsation IVMGuestOS (VPCCOMInterfaces. h)
description: Determina se a máquina virtual tem uma pulsação.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- PC virtual de propriedade ispulsação
- Propriedade ispulsação Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, ispulsação de propriedade
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
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105783720"
---
# <a name="ivmguestosisheartbeating-property"></a>Propriedade IVMGuestOS:: ispulsação

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se a máquina virtual tem uma pulsação.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Valor da propriedade

**Variante \_ TRUE** se uma pulsação for detectada, **variante \_ false** caso contrário.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                              | Significado                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | A operação foi bem-sucedida.<br/>                                                                                                                         |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                   | O parâmetro é **NULL**.<br/>                                                                                                                            |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>           | A configuração é desconhecida.<br/>                                                                                                                         |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>      | A máquina virtual deve estar em execução para esta operação.<br/>                                                                                               |
| <dl> <dt>VM \_ E \_ adições \_ não \_ </dt> <dt>0xA0040504</dt> disp. </dl> | A máquina virtual não está totalmente inicializada, o recurso componentes de integração não está instalado ou a versão instalada não oferece suporte a esse recurso.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>           | Ocorreu um erro inesperado.<br/>                                                                                                                     |



## <a name="remarks"></a>Comentários

Quando os componentes de integração são instalados no sistema operacional convidado, um ' tique ' regular ou pulsação é enviado da sessão de máquina virtual para o Windows Virtual PC. Se o sistema operacional convidado estiver muito carregado, será possível que o Virtual PC receba menos pulsações do que o esperado. Se nenhuma pulsação for detectada, é possível que o sistema operacional convidado não esteja respondendo ou tenha falhado.

Por padrão, uma máquina virtual produz dez tiques de pulsação por minuto. Se nenhuma marcação de pulsação for detectada por um minuto inteiro, o Windows Virtual PC tentará reiniciar a sessão da máquina virtual uma vez a cada dez segundos por até dois minutos. Esse comportamento é controlado pelos seguintes valores de chave no arquivo de configuração da sessão da máquina virtual.



| Chave de configuração                                            | Padrão       | Descrição                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| integração/Microsoft/pulsação/tempo<br/>              | 60<br/> | O comprimento do bloco de tempo usado para gerar tiques de pulsação, em em segundos.<br/>                                             |
| integração/Microsoft/pulsação/taxa<br/>              | 10<br/> | O número de tiques gerados em cada bloco de tempo de pulsação.<br/>                                                                  |
| integração/Microsoft/intervalo de pulsação/falha \_<br/> | 10<br/> | O número de segundos entre as tentativas de reinicialização, uma vez que nenhuma marcação de pulsação é recebida dentro de um bloco de tempo de pulsação específico.<br/> |
| integração/Microsoft/falhas de pulsação \_ /falha<br/> | 12<br/> | O número de tentativas de reinicialização feitas.<br/>                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

