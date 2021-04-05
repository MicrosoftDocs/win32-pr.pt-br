---
title: Método Mergeto IVMHardDisk (VPCCOMInterfaces. h)
description: Mescla um disco rígido virtual diferencial com todos os seus pais.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- PC virtual do método Mergeto
- Método Mergeto Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, método Mergeto
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085651"
---
# <a name="ivmharddiskmergeto-method"></a>Método IVMHardDisk:: Mergeto

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Mescla um disco rígido virtual diferencial com todos os seus pais (até e incluindo o disco rígido virtual pai raiz) em um novo arquivo de disco rígido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newDiskImagePath* \[ no\]
</dt> <dd>

O caminho para a nova imagem de disco de destino em que as imagens de disco selecionadas serão mescladas.

</dd> <dt>

*newDiskImageType* \[ no\]
</dt> <dd>

O tipo de imagem do novo disco de destino. Os tipos de imagem permitidos para a nova imagem de disco de destino são **vmDiskType \_ Dynamic** e **vmDiskType \_ FixedSize**. Para obter mais informações, consulte [**VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de mesclagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                      | Um parâmetro é **nulo**.<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | O parâmetro *newDiskImagePath* está vazio.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt> </dl>   | O sistema não pode localizar o arquivo especificado pelo parâmetro *newDiskImagePath* .<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt> </dl>   | O sistema não pode localizar o caminho especificado pelo parâmetro *newDiskImagePath* .<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>      | O parâmetro *newDiskImagePath* contém um caractere inválido (um dos seguintes: " \* ? <>/ \| ": ").<br/>                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>      | O parâmetro *newDiskImagePath* especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                                                                                                                                                                                                |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | O caminho especificado pelo parâmetro *newDiskImagePath* é muito longo. O caminho deve ter menos de 260 caracteres.<br/>                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt> </dl> | O disco rígido virtual referenciado por este objeto está em uso ou o pai deste disco rígido virtual está em uso.<br/>                                                                                                                                                                                |
| <dl> <dt>**VM \_ E \_ \_ tipo de \_ imagem \_ HD incorreto**</dt> <dt>0xA004067B</dt> </dl>                   | Esse erro é causado porque a imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) não é uma imagem de disco diferencial ou porque o parâmetro *newDiskImageType* não é um dos valores aceitos, **vmDiskType \_ Dynamic** ou **vmDiskType \_ FixedSize**.<br/> |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt> </dl>    | O arquivo referenciado pelo parâmetro *newDiskImagePath* já existe.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt> </dl>         | O volume do host não tem espaço suficiente para mesclar este disco rígido virtual.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**VM \_ E \_ \_ caminho pai \_ não \_ encontrado**</dt> <dt>0xA0040677</dt> </dl>                 | O pai do disco rígido virtual referenciado por este objeto não existe.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt> </dl>                      | A imagem do disco rígido virtual não pode ser mesclada porque o aplicativo está sendo desligado.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                              | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

