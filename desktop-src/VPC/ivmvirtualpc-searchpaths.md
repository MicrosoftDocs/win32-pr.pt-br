---
title: Propriedade SearchPaths IVMVirtualPC (VPCCOMInterfaces.h)
description: Caminhos do sistema de arquivos usados para encontrar arquivos associados ao Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- Propriedade SearchPaths Pc Virtual
- Propriedade SearchPaths Pc Virtual , interface IVMVirtualPC
- INTERFACE IVMVirtualPC PC virtual, propriedade SearchPaths
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ef75bf0a696494b839f330063ca310927a0d796829d96575721f492b8b691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471246"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>Propriedade IVMVirtualPC::SearchPaths

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define os caminhos do sistema de arquivos usados para encontrar arquivos associados ao Windows Virtual PC.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica uma safearray que contém um caminho do sistema de arquivos para cada entrada.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                               | Significado                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                               |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                                    | O parâmetro é **NULL.**<br/>                                                                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                                 | O *parâmetro searchPaths* não é válido e não pôde ser analisado em uma matriz de caminhos.<br/>                                    |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0X80070002</dt> </dl> | O sistema não pode encontrar um diretório especificado no *parâmetro searchPaths.*<br/>                                                |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)</dt> <dt>0X80070003</dt> </dl> | O sistema não pode encontrar um caminho especificado pelo *parâmetro searchPaths.*<br/>                                                     |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)</dt> <dt>0X8007007B</dt> </dl>    | Um caminho especificado no parâmetro *searchPaths* contém caracteres ilícitos. Os caracteres ilícitos são " \* ?<>/ \| ":".<br/> |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ \_ BAD PATHNAME)</dt> <dt>0x800700a1</dt> </dl>    | Um caminho contido no parâmetro *searchPaths* especifica um caminho vazio ou relativo. Um caminho absoluto é necessário.<br/>          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt> </dl> | O caminho especificado no parâmetro *searchPaths* é muito longo. O comprimento do caminho deve ter menos de 260 caracteres.<br/>     |
| <dl> <dt>VM \_ E \_ PREF \_ NÃO ENCONTRADO \_ 0XA0040300</dt> <dt></dt> </dl>                       | A preferência não foi encontrada.<br/>                                                                                               |
| <dl> <dt>VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA</dt> <dt>0XA0040951</dt> </dl>     | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/>                                        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

