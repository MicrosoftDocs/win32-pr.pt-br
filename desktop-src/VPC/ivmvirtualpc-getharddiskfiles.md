---
title: Método IVMVirtualPC GetHardDiskFiles (VPCCOMInterfaces.h)
description: Recupera uma matriz de arquivos de disco rígido virtuais conhecidos.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Pc Virtual do método GetHardDiskFiles
- Método GetHardDiskFiles Pc Virtual, interface IVMVirtualPC
- INTERFACE IVMVirtualPC pc virtual , método GetHardDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 902cd124db27ae65b8f589ded8b2b3188a7e0df67b0ff20071abd04daf5ab894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136569"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a>Método IVMVirtualPC::GetHardDiskFiles

\[O Computador Virtual do Windows não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma matriz de arquivos de disco rígido virtuais conhecidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inAdditionalSearchPaths* \[ Em\]
</dt> <dd>

Esses caminhos serão pesquisados junto com os caminhos definidos na [**propriedade IVMVirtualPC::SearchPaths.**](ivmvirtualpc-searchpaths.md)

</dd> <dt>

*outHardDiskFileList* \[ out, retval\]
</dt> <dd>

Uma matriz de cadeias de caracteres de caminho para os arquivos de disco rígido virtual encontrados nos caminhos de pesquisa especificados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                | O *parâmetro outHardDiskFileList* é **NULL.**<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | O *parâmetro inAdditionalSearchPaths* não é uma matriz de cadeias de caracteres.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>**VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA**</dt> <dt>0XA0040951</dt> </dl> | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/> |



 

## <a name="remarks"></a>Comentários

Os caminhos de pesquisa usados para recuperar a matriz de arquivos incluirão aqueles definidos anteriormente por [**IVMVirtualPC::SearchPaths,**](ivmvirtualpc-searchpaths.md) além daqueles especificados pelo parâmetro *inAdditionalSearchPaths.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos \[ da área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

