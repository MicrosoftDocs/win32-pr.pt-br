---
title: Método IVMVirtualPC CreateDynamicVirtualHardDisk (VPCCOMInterfaces.h)
description: Cria um disco rígido virtual de reizing dinamicamente.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- Pc Virtual do método CreateDynamicVirtualHardDisk
- Método CreateDynamicVirtualHardDisk pc virtual, interface IVMVirtualPC
- INTERFACE IVMVirtualPC Pc Virtual , método CreateDynamicVirtualHardDisk
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
ms.openlocfilehash: 6de505f2e8b47bc36b7537a3abcdab1f07e7551a8c5ed9caee9aed100288df51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998646"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a>Método IVMVirtualPC::CreateDynamicVirtualHardDisk

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Cria um disco rígido virtual de reizing dinamicamente.

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

*imagePath* \[ Em\]
</dt> <dd>

O caminho completo para o novo arquivo de imagem de disco. A pasta que contém será criada se ela não existir.

</dd> <dt>

*tamanho* \[ Em\]
</dt> <dd>

O tamanho da imagem, em megabytes. Esse valor pode ser no máximo 2.088.960 MB (2040 GB).

</dd> <dt>

*diskTask* \[ out, retval\]
</dt> <dd>

Um [**objeto IVMTask**](ivmtask.md) usado para acompanhar a criação da imagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                       |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                    | Um parâmetro é **NULL.**<br/>                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | O *parâmetro* de tamanho é menor ou igual a 0.<br/>                                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0X80070003</dt> </dl> | O sistema não pode encontrar o caminho especificado pelo *parâmetro imagePath.*<br/>                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ DRIVE)**</dt> <dt>0X8007000F</dt> </dl>   | O arquivo especificado pelo parâmetro *imagePath* está em um CD-ROM ou DVD-ROM.<br/>                                                                                                                                                          |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0X8007007B</dt> </dl>    | O *parâmetro imagePath* contém um caractere inválido (um de " \* ?:<>/ \| "").<br/>                                                                                                                                                |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ BAD PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *imagePath* especifica um caminho vazio ou relativo. Pelo menos um dos parâmetros deve ser um caminho absoluto.<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0X8007006F</dt> </dl> | O caminho especificado pelo parâmetro *imagePath* é muito longo. O comprimento do caminho deve ter menos de 260 caracteres.<br/>                                                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ ALREADY EXISTS)**</dt> <dt>0X800700B7</dt> </dl>  | O arquivo referenciado pelo *parâmetro imagePath* já existe.<br/>                                                                                                                                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0X80070070</dt> </dl>       | A imagem de disco rígido virtual de expansão dinâmica precisa de pelo menos 8 MB de livre no volume do host.<br/>                                                                                                                                      |
| <dl> <dt>**VM \_ TAMANHO \_ DA IMAGEM E MUITO \_ \_ \_ GRANDE**</dt> <dt>0XA0040683</dt> </dl>                | O tamanho *do* parâmetro deve ser menor que 2.088.960 MB. Se o formato for FAT16, o tamanho deverá ser menor que 2000 MB.<br/>                                                                                                                   |
| <dl> <dt>**VM \_ TAMANHO \_ DA IMAGEM E MUITO PEQUENO \_ \_ \_ 0XA0040684**</dt> <dt></dt> </dl>                | As imagens de disco rígido virtual não formatadas e fat16 devem ter pelo menos 3 MB. As imagens de disco rígido virtual formatadas em FAT32 devem ter pelo menos 514 MB.<br/>                                                                                   |
| <dl> <dt>**VM \_ ARQUIVO \_ E MUITO GRANDE PARA \_ \_ \_ \_ VOLUME**</dt> <dt>0XA0040679</dt> </dl>          | O volume do host não poderá dar suporte a um arquivo desse tamanho se a imagem de disco rígido virtual de expansão dinâmica expandir para seu limite total. O tamanho máximo do arquivo para um volume FAT32 é de 4 GB. O tamanho máximo do arquivo para um volume FAT16 é de 2 GB.<br/> |
| <dl> <dt>**VM \_ E \_ O APLICATIVO ESTÁ \_ \_ DESLIGANDO**</dt> <dt>0XA0040209</dt> </dl>                    | O disco rígido virtual não pode ser criado depois que o aplicativo começa a ser desligado.<br/>                                                                                                                                            |
| <dl> <dt>**VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA**</dt> <dt>0XA0040951</dt> </dl>     | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/>                                                                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

