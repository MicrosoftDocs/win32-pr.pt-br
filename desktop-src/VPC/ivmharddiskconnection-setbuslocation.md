---
title: Método IVMHardDiskConnection SetBusLocation (VPCCOMInterfaces. h)
description: Define o local do barramento ao qual este disco rígido está anexado.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- SetBusLocation do método virtual PC
- Método SetBusLocation Virtual PC, interface IVMHardDiskConnection
- IVMHardDiskConnection interface virtual PC, método SetBusLocation
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294751"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a>Método IVMHardDiskConnection:: SetBusLocation

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define o local do barramento ao qual este disco rígido está anexado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vmBusNumber* \[ no\]
</dt> <dd>

O número do barramento a ser usado.

</dd> <dt>

*vmDeviceNumber* \[ no\]
</dt> <dd>

O número do dispositivo a ser usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                               | Descrição                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | A operação foi bem-sucedida.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | O local do barramento especificado não é válido.<br/>                                                         |
| <dl> <dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt> </dl>    | Não foi possível definir o local do barramento porque a máquina virtual está em um estado em execução ou salvo.<br/>    |
| <dl> <dt>**VM \_ \_ \_ Barramento de unidade E \_ loc \_ in \_ usar**</dt> <dt>0xA00400503</dt> </dl> | O local do barramento não pôde ser definido porque outro dispositivo está conectado no momento a este local.<br/> |
| <dl> <dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt> </dl>            | A unidade atual não é válida.<br/>                                                                  |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>               | A máquina virtual atual não é válida.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>               | Ocorreu um erro inesperado.<br/>                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection é definido como aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

