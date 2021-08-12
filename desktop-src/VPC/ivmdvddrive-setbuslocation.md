---
title: Método IVMDVDDrive SetBusLocation (VPCCOMInterfaces. h)
description: Anexa a unidade de DVD ao local do barramento especificado na máquina virtual.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- SetBusLocation do método virtual PC
- Método SetBusLocation Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 593a42c21d1ed688185a7fe7123e972998859c010775a2cf4efd5f3bbbbaa98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595839"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>Método IVMDVDDrive:: SetBusLocation

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa a unidade de DVD ao local do barramento especificado na máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*busNumber* \[ no\]
</dt> <dd>

O número do barramento ao qual esta unidade deve ser anexada. Por exemplo, em um barramento IDE, esse número representaria se o número de barramento primário ou secundário deve ser usado.

</dd> <dt>

*deviceNumber* \[ no\]
</dt> <dd>

O número do dispositivo ao qual esta unidade deve ser anexada. Por exemplo, em um barramento IDE, esse número representaria se o local do dispositivo primário ou secundário deve ser usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                            | Descrição                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | A operação foi bem-sucedida.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                 | O local do barramento especificado não é válido.<br/>                                                                                     |
| <dl> <dt>**E \_ FALHA**</dt> <dt>0x80004005</dt> </dl>                       | Ocorreu um erro inesperado.<br/>                                                                                            |
| <dl> <dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt> </dl> | O local do barramento não pode ser definido enquanto a máquina virtual está em execução ou está em um estado salvo.<br/>                                     |
| <dl> <dt>**\_E/ \_ s \_ de barramento da VM \_ em \_ uso**</dt> </dl>                                                                      | Outro dispositivo já está conectado ao local do barramento especificado.<br/>                                                            |
| <dl> <dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt> </dl>         | A unidade atual não pôde ser inicializada.<br/>                                                                                  |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>            | Não foi possível gravar as alterações no arquivo de preferências porque a máquina virtual desta unidade não pôde ser determinada.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>            | Ocorreu um erro inesperado.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

