---
title: Método IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces. h)
description: Adiciona uma nova conexão de disco rígido à máquina virtual.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- AddHardDiskConnection do método virtual PC
- Método AddHardDiskConnection Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748734"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>Método IVMVirtualMachine:: AddHardDiskConnection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Adiciona uma nova conexão de disco rígido à VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hardDiskPath* \[ no\]
</dt> <dd>

O caminho completo do arquivo de disco rígido virtual (VHD) a ser conectado.

</dd> <dt>

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

*hardDiskConnection* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                              | Descrição                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | A operação foi bem-sucedida.<br/>                                                                                                                  |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                      | O parâmetro *hardDiskConnection* é **nulo**.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | Um parâmetro *hardDiskPath* é **nulo** ou o parâmetro *busNumber* ou *deviceNumber* não é válido.<br/>                                            |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt> </dl>   | O sistema não pode localizar o arquivo especificado pelo parâmetro *hardDiskPath* .<br/>                                                                     |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt> </dl>   | O sistema não pode localizar o caminho especificado pelo parâmetro *hardDiskPath* .<br/>                                                                     |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>      | O parâmetro *hardDiskPath* contém um caractere inválido (um de " \* ? <>/ \| ": ").<br/>                                                        |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>      | O parâmetro *hardDiskPath* especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                                                |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | O caminho especificado pelo parâmetro *hardDiskPath* é muito longo. O caminho deve ter menos de 260 caracteres.<br/>                                     |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                              | A configuração é desconhecida.<br/>                                                                                                                  |
| <dl> <dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt> </dl>                   | A VM está em um estado em execução ou salvo.<br/>                                                                                                         |
| <dl> <dt>**VM \_ \_ \_ Barramento de unidade E \_ loc \_ in \_ usar**</dt> <dt>0xA00400503</dt> </dl>                | O local do barramento especificado está em uso.<br/>                                                                                                          |
| <dl> <dt>**VM \_ E \_ \_ \_ arquivo HD inválido**</dt> <dt>0xA0040682</dt> </dl>                        | O VHD é maior que 127 GB e não pode ser conectado ao barramento IDE.<br/>                                                                         |
| <dl> <dt>**VM \_ E \_ \_ \_ \_ tipo de disco HD sem suporte**</dt> <dt>0xA00400686</dt> </dl>             | O parâmetro *hardDiskPath* refere-se a um VHD vinculado ou a um VHD diferencial para um VHD vinculado. VHDs vinculados não podem ser anexados a máquinas virtuais.<br/> |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt> </dl> | O VHD especificado já está conectado a outro local de barramento para esta VM.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                              | Ocorreu um erro inesperado.<br/>                                                                                                              |



 

## <a name="remarks"></a>Comentários

Você só pode adicionar uma nova conexão de disco rígido a uma máquina virtual parada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

