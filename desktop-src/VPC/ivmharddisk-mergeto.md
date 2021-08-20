---
title: Método IVMHardDisk MergeTo (VPCCOMInterfaces.h)
description: Mescla um disco rígido virtual diferencial com todos os seus pais.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Pc Virtual do método MergeTo
- Pc Virtual do método MergeTo, interface IVMHardDisk
- INTERFACE IVMHardDisk pc virtual , método MergeTo
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
ms.openlocfilehash: 19f54c3e7cfcd328adcea355e90ff60d92590fb694915a3e682a6240b656e655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123706"
---
# <a name="ivmharddiskmergeto-method"></a>Método IVMHardDisk::MergeTo

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*newDiskImagePath* \[ Em\]
</dt> <dd>

O caminho para a nova imagem de disco de destino em que as imagens de disco selecionadas serão mescladas.

</dd> <dt>

*newDiskImageType* \[ Em\]
</dt> <dd>

O tipo de nova imagem de disco de destino. Os tipos de imagem permitidos para a nova imagem de disco de destino **são vmDiskType \_ Dynamic** **e vmDiskType \_ FixedSize**. Para obter mais informações, [**consulte VMHardDiskType**](vmharddisktype.md).

</dd> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Um [**objeto IVMTask**](ivmtask.md) usado para acompanhar a conclusão do processo de mesclamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                      | Um parâmetro é **NULL.**<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | O *novo parâmetroDiskImagePath* está vazio.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0X80070002</dt> </dl>   | O sistema não pode encontrar o arquivo especificado pelo *novo parâmetroDiskImagePath.*<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0X80070003</dt> </dl>   | O sistema não pode encontrar o caminho especificado pelo *parâmetro newDiskImagePath.*<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0X8007007B</dt> </dl>      | O *novo parâmetroDiskImagePath* contém um caractere inválido (um dos seguintes: " \* ?<>/ \| ":").<br/>                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ BAD PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | O *parâmetro newDiskImagePath* especifica um caminho vazio ou relativo. Um caminho absoluto é necessário.<br/>                                                                                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0X8007006F</dt> </dl>   | O caminho especificado pelo novo *parâmetroDiskImagePath* é muito longo. O caminho deve ter menos de 260 caracteres.<br/>                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0X80070020</dt> </dl> | O disco rígido virtual referenciado por esse objeto está em uso ou o pai desse disco rígido virtual está em uso.<br/>                                                                                                                                                                                |
| <dl> <dt>**VM \_ E \_ TIPO DE IMAGEM HD ERRADO \_ \_ \_ 0XA004067B**</dt> <dt></dt> </dl>                   | Esse erro é causado porque a imagem de disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) não é uma imagem de disco diferencial ou porque o parâmetro *newDiskImageType* não é um dos valores aceitos, **vmDiskType \_ Dynamic** ou **vmDiskType \_ FixedSize**.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ ALREADY EXISTS)**</dt> <dt>0X800700B7</dt> </dl>    | O arquivo referenciado pelo *novo parâmetroDiskImagePath* já existe.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0X80070070</dt> </dl>         | O volume do host não tem espaço suficiente para mesclar esse disco rígido virtual.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**VM \_ E \_ CAMINHO PAI NÃO ENCONTRADO \_ \_ \_ 0XA0040677**</dt> <dt></dt> </dl>                 | O pai do disco rígido virtual referenciado por esse objeto não existe.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**VM \_ E \_ O APLICATIVO ESTÁ \_ \_ DESLIGANDO**</dt> <dt>0XA0040209</dt> </dl>                      | A imagem do disco rígido virtual não pode ser mesclada porque o aplicativo está sendo desligado.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk é definido como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

