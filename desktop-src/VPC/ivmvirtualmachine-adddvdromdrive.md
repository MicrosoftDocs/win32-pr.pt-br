---
title: Método IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces. h)
description: Adiciona uma nova unidade de CD ou DVD à máquina virtual.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- AddDVDROMDrive do método virtual PC
- Método AddDVDROMDrive Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método AddDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a875af50d38270b898c17f2848a4e4b33fe79a4b17d9ab7b6be58cdcfcf92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123226"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a>Método IVMVirtualMachine:: AddDVDROMDrive

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Adiciona uma nova unidade de CD ou DVD à máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*busNumber* \[ no\]
</dt> <dd>

O barramento ao qual a unidade será anexada.



| Valor                                                                        | Significado                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | A unidade será anexada ao primeiro barramento.<br/>  |
| <dl> <dt>1</dt> </dl> | A unidade será anexada ao segundo barramento.<br/> |



 

</dd> <dt>

*deviceNumber* \[ no\]
</dt> <dd>

O dispositivo ao qual a unidade será anexada.



| Valor                                                                        | Significado                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | A unidade será anexada ao primeiro dispositivo no barramento.<br/>  |
| <dl> <dt>1</dt> </dl> | A unidade será anexada ao segundo dispositivo no barramento.<br/> |



 

</dd> <dt>

*dvdDrive* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMDVDDrive**](ivmdvddrive.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                               | Descrição                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | A operação foi bem-sucedida.<br/>                       |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                       | O parâmetro *dvdDrive* é **nulo**.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | Um parâmetro não é válido.<br/>                           |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>               | A configuração é desconhecida.<br/>                       |
| <dl> <dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt> </dl>    | A máquina virtual está em um estado em execução ou salvo.<br/> |
| <dl> <dt>**VM \_ \_ \_ Barramento de unidade E \_ loc \_ in \_ usar**</dt> <dt>0xA00400503</dt> </dl> | O local do barramento especificado está em uso.<br/>               |
| <dl> <dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt> </dl>            | A unidade especificada não é válida.<br/>                   |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>               | Ocorreu um erro inesperado.<br/>                   |



 

## <a name="remarks"></a>Comentários

Você só pode adicionar uma nova unidade de CD ou DVD a uma máquina virtual parada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

