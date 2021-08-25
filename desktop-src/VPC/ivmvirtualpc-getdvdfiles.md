---
title: Método IvMVirtualPC GetDVDFiles (VPCCOMInterfaces.h)
description: Recupera uma matriz de arquivos de DVD conhecidos.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- Pc Virtual do método GetDVDFiles
- Método GetDVDFiles pc virtual, interface IVMVirtualPC
- INTERFACE IVMVirtualPC pc virtual , método GetDVDFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 585b1558c5a0692d4f9a3d5d8371cd0b7e5a692596c06605e7d86eadf377cf45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864116"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a>Método IVMVirtualPC::GetDVDFiles

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma matriz de arquivos de DVD conhecidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inAdditionalSearchPaths* \[ Em\]
</dt> <dd>

Esses caminhos serão pesquisados junto com os caminhos definidos na [**propriedade IVMVirtualPC::SearchPaths.**](ivmvirtualpc-searchpaths.md)

</dd> <dt>

*outDVDFileList* \[ out, retval\]
</dt> <dd>

Uma matriz de arquivos de DVD virtual encontrados nos caminhos de pesquisa especificados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                | O *parâmetro outDVDFileList* é **NULL.**<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | O *parâmetro inAdditionalSearchPaths* não é uma matriz de cadeias de caracteres.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>**VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA**</dt> <dt>0XA0040951</dt> </dl> | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/> |



 

## <a name="remarks"></a>Comentários

Os caminhos de pesquisa usados para recuperar a matriz de arquivos incluirão aqueles definidos anteriormente por [**IVMVirtualPC::SearchPaths,**](ivmvirtualpc-searchpaths.md) além daqueles especificados pelo parâmetro *inAdditionalSearchPaths* e o local do instalador para o módulo de componentes de integração.

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

 

