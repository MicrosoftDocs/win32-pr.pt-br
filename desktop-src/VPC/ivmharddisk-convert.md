---
title: Método Convert de IVMHardDisk (VPCCOMInterfaces. h)
description: Converte um disco rígido virtual de tamanho fixo em um disco rígido virtual de expansão dinâmica ou converte um disco rígido virtual de expansão dinâmica em um disco rígido virtual de tamanho fixo.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Converter o método virtual PC
- Converter método virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Método Convert
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e509c683ef86e169eb07d661c9682d8ed67204bcc7e1651d2d6370ee4be82f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593879"
---
# <a name="ivmharddiskconvert-method"></a>Método IVMHardDisk:: Convert

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Converte um disco rígido virtual de tamanho fixo em um disco rígido virtual de expansão dinâmica ou converte um disco rígido virtual de expansão dinâmica em um disco rígido virtual de tamanho fixo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*convertedDiskImagePath* \[ no\]
</dt> <dd>

O caminho para o arquivo de imagem de disco de destino.

</dd> <dt>

*convertedDiskImageType* \[ no\]
</dt> <dd>

O tipo da imagem do disco de destino. Para obter uma lista de valores, consulte [**VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*convertTask* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de conversão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                              | Descrição                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | A operação foi bem-sucedida.<br/>                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | O parâmetro *convertedDiskImagePath* está vazio ou não tem a extensão. vhd no nome do arquivo.<br/>                                      |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                      | Um parâmetro é **nulo**.<br/>                                                                                                             |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt> </dl>   | O sistema não pode localizar o caminho especificado pelo parâmetro *convertedDiskImagePath* .<br/>                                                 |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>      | O parâmetro *convertedDiskImagePath* contém um caractere inválido (um de " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>      | O parâmetro *convertedDiskImagePath* especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                            |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl>   | O caminho especificado pelo parâmetro *convertedDiskImagePath* é muito longo. O caminho deve ser menor que **o \_ caminho máximo** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt> </dl> | O disco rígido virtual referenciado por este objeto está em uso ou o pai deste disco rígido virtual está em uso.<br/>                  |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt> </dl>         | O volume do host não tem espaço suficiente para converter este disco rígido virtual.<br/>                                                        |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt> </dl>    | O arquivo referenciado pelo parâmetro *convertedDiskImagePath* já existe.<br/>                                                        |
| <dl> <dt>**VM \_ E \_ \_ tipo de \_ imagem \_ HD incorreto**</dt> <dt>0xA004067B</dt> </dl>                   | O parâmetro *convertedDiskImagePath* deve ser **VmDiskType \_ dinâmico** ou **vmDiskType \_ FixedSize**.<br/>                          |
| <dl> <dt>**VM \_ E \_ \_ \_ arquivo HD inválido**</dt> <dt>0xA0040682</dt> </dl>                        | A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) não parece ser uma imagem válida.<br/>          |
| <dl> <dt>**VM \_ E \_ \_ caminho pai \_ não \_ encontrado**</dt> <dt>0xA0040677</dt> </dl>                 | O pai do disco rígido virtual referenciado por este objeto não existe.<br/>                                                        |
| <dl> <dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt> </dl>                      | A imagem do disco rígido virtual não pode ser convertida porque o aplicativo está sendo desligado.<br/>                                            |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                              | Ocorreu um erro inesperado.<br/>                                                                                                    |



 

## <a name="remarks"></a>Comentários

O arquivo de origem permanece intacto após o processo de conversão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

