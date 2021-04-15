---
title: Método IVMVirtualPC CreateDynamicVirtualHardDisk (VPCCOMInterfaces. h)
description: Cria um disco rígido virtual de redimensionamento dinâmico.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- CreateDynamicVirtualHardDisk do método virtual PC
- Método CreateDynamicVirtualHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método CreateDynamicVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d245072fd5b3135decd814a29dd8a87d2b6a956
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369922"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a>Método IVMVirtualPC:: CreateDynamicVirtualHardDisk

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Cria um disco rígido virtual de redimensionamento dinâmico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateDynamicVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*imagePath* \[ no\]
</dt> <dd>

O caminho completo para o novo arquivo de imagem de disco. A pasta que a contém será criada se não existir.

</dd> <dt>

*tamanho* \[ no\]
</dt> <dd>

O tamanho da imagem, em megabytes. Esse valor pode ter no máximo 2.088.960 MB (2040GB).

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a criação da imagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | Um parâmetro é **nulo**.<br/>                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | O parâmetro *size* é menor ou igual a 0.<br/>                                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt> </dl> | O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* .<br/>                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (unidade de erro \_ inválida \_ )**</dt> <dt>0x8007000f</dt> </dl>   | O arquivo especificado pelo parâmetro *imagePath* está em um CD-ROM ou DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>    | O parâmetro *imagePath* contém um caractere inválido (um de " \* ?: <>/ \| " ").<br/>                                                                                                                                                |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *imagePath* especifica um caminho relativo ou vazio. Pelo menos um dos parâmetros deve ser um caminho absoluto.<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | O caminho especificado pelo parâmetro *imagePath* é muito longo. O comprimento do caminho deve ter menos de 260 caracteres.<br/>                                                                                                               |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt> </dl>  | O arquivo referenciado pelo parâmetro *imagePath* já existe.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt> </dl>       | A imagem de disco rígido virtual de expansão dinâmica precisa de pelo menos 8 MB livres no volume do host.<br/>                                                                                                                                      |
| <dl> <dt>**VM \_ \_Tamanho da imagem E \_ \_ muito \_ grande**</dt> <dt>0xA0040683</dt> </dl>                | O *tamanho* do parâmetro deve ser menor que 2.088.960 MB. Se o formato for FAT16, o tamanho deverá ser menor que 2000 MB.<br/>                                                                                                                   |
| <dl> <dt>**VM \_ \_Tamanho da imagem E \_ \_ muito \_ pequeno**</dt> <dt>0xA0040684</dt> </dl>                | As imagens de disco rígido virtual formatado e FAT16 não formatados devem ter pelo menos 3 MB. As imagens de disco rígido virtual formatado para FAT32 devem ter pelo menos 514 MB.<br/>                                                                                   |
| <dl> <dt>**VM \_ \_Arquivo E \_ muito \_ grande \_ para o \_ volume**</dt> <dt>0xA0040679</dt> </dl>          | O volume do host não poderá dar suporte a um arquivo esse tamanho se a imagem do disco rígido virtual de expansão dinâmica expandir para seu limite completo. O tamanho máximo do arquivo para um volume FAT32 é 4 GB. O tamanho máximo do arquivo para um volume FAT16 é 2 GB.<br/> |
| <dl> <dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt> </dl>                    | O disco rígido virtual não pode ser criado depois que o aplicativo inicia o desligamento.<br/>                                                                                                                                            |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl>     | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

