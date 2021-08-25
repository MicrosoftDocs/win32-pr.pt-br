---
description: A interface IPortableDeviceValues contém uma coleção de pares PROPERTYKEY/PROPVARIANT.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: Interface IPortableDeviceValues (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7f7aaceff66cd817666dd05b92243239f860b2f59a993e4afca1831fc8085de0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929996"
---
# <a name="iportabledevicevalues-interface"></a>Interface IPortableDeviceValues

A interface **IPortableDeviceValues** contém uma coleção de pares de PROPVARIANT de **PROPERTYKEY** /  . Os valores na coleção não precisam ser do mesmo VARTYPE.

Os valores são armazenados como pares chave-valor; cada chave deve ser exclusiva na coleção. Os clientes podem pesquisar itens por **PROPERTYKEY** ou por índice baseado em zero. Os valores de dados são armazenados como estruturas **PROPVARIANT** . Você pode adicionar ou recuperar valores de qualquer tipo usando os métodos genéricos **SetValue** e **GetValue**, ou você pode adicionar itens usando o método específico para o tipo de dados adicionado.

Os métodos **Get...** exigem que o chamador libere quaisquer valores recuperados adequadamente. Os métodos **set...** copiam o valor na coleção.

Quando uma interface **IPortableDeviceValues** é liberada, ela chama **Clear**, que libera a memória que foi alocada para todos os seus membros adequadamente.

Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chame **CoCreate** com **CLSID \_ PortableDeviceValues**.

## <a name="members"></a>Membros

A interface **IPortableDeviceValues** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceValues** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IPortableDeviceValues** tem esses métodos.



| Método                                                                                                                     | Descrição                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Limpar**](iportabledevicevalues-clear.md)                                                                               | Exclui todos os itens da coleção.<br/>                                                                      |
| [**CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Copia o conteúdo de um **IPropertyStore** na coleção.<br/>                                           |
| [**CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Copia todos os valores de uma coleção para uma interface **IPropertyStore** .<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Recupera um valor da coleção usando o índice de base zero fornecido.<br/>                                  |
| [**Getboolvalue**](iportabledevicevalues-getboolvalue.md)                                                                 | Recupera um valor **bool** (tipo VT \_ bool) especificado por uma chave.<br/>                                              |
| [**Getbuffervalue**](iportabledevicevalues-getbuffervalue.md)                                                             | Recupera um valor de matriz de bytes (tipo VT \_ vector \| VT \_ UI1) especificado por uma chave.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Recupera o número de itens na coleção.<br/>                                                            |
| [**GetError**](iportabledevicevalues-geterrorvalue.md)                                                               | Recupera um valor **HRESULT** (erro de tipo VT \_ ) especificado por uma chave.<br/>                                         |
| [**Getfloatvalue**](iportabledevicevalues-getfloatvalue.md)                                                               | Recupera um valor **float** (tipo VT \_ R4) especificado por uma chave.<br/>                                               |
| [**Getguidvalue**](iportabledevicevalues-getguidvalue.md)                                                                 | Recupera um valor de **GUID** (tipo VT \_ CLSID) especificado por uma chave.<br/>                                             |
| [**GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Recupera um valor de **IPortableDeviceKeyCollection** (tipo VT \_ desconhecido) especificado por uma chave.<br/>                  |
| [**GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Recupera um valor de **IPortableDevicePropVariantCollection** (tipo VT \_ desconhecido) especificado por uma chave.<br/>          |
| [**GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Recupera um valor de **IPortableDeviceValuesCollection** (tipo VT \_ desconhecido) especificado por uma chave.<br/>               |
| [**GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Recupera um valor de **IPortableDeviceValues** (tipo VT \_ desconhecido) especificado por uma chave.<br/>                         |
| [**Getiunknownvalue**](iportabledevicevalues-getiunknownvalue.md)                                                         | Recupera um valor de interface **IUnknown** (tipo VT \_ desconhecido) especificado por uma chave.<br/>                            |
| [**GetKeyValue**](iportabledevicevalues-getkeyvalue.md)                                                                   | Recupera um valor de **PROPERTYKEY** especificado por uma chave.<br/>                                                       |
| [**GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)                                               | Recupera um valor **longo** (tipo VT \_ i4) especificado por uma chave.<br/>                                                |
| [**GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Recupera um valor de **LONGLONG** (tipo VT \_ i8) especificado por uma chave.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Recupera um valor de cadeia de caracteres (tipo VT \_ LPWSTR) especificado por uma chave.<br/>                                              |
| [**GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Recupera um valor **ULONG** (tipo VT \_ UI4) especificado por uma chave.<br/>                                              |
| [**GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Recupera um valor de **ULONGLONG** (tipo VT \_ UI8) especificado por uma chave.<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | Recupera um valor de **PROPVARIANT** especificado por uma chave.<br/>                                                       |
| [**Remover removida**](iportabledevicevalues-removevalue.md)                                                                   | Remove um item da coleção.<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | Adiciona um novo valor **booliano** (tipo VT \_ bool) ou substitui um existente.<br/>                                 |
| [**Setbuffervalue**](iportabledevicevalues-setbuffervalue.md)                                                             | Adiciona um novo valor de **byte** \* (tipo VT \_ vector \| VT \_ UI1) ou substitui um existente.<br/>                     |
| [**SetError**](iportabledevicevalues-seterrorvalue.md)                                                               | Adiciona um novo valor **HRESULT** (erro de tipo VT \_ ) ou substitui um existente.<br/>                                |
| [**Setfloatvalue**](iportabledevicevalues-setfloatvalue.md)                                                               | Adiciona um novo valor **float** (tipo VT \_ R4) ou substitui um existente.<br/>                                     |
| [**Setguidvalue**](iportabledevicevalues-setguidvalue.md)                                                                 | Adiciona um novo valor de **GUID** (tipo VT \_ CLSID) ou substitui um existente.<br/>                                   |
| [**SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Adiciona um novo valor de **IPortableDeviceKeyCollectionValue** (tipo VT \_ desconhecido) ou substitui um existente.<br/>    |
| [**SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Adiciona um novo valor de **IPortableDevicePropVariantCollection** (tipo VT \_ desconhecido) ou substitui um existente.<br/> |
| [**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Adiciona um novo valor de **IPortableDeviceValuesCollection** (tipo VT \_ desconhecido) ou substitui um existente.<br/>      |
| [**SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Adiciona um novo valor de **IPortableDeviceValues** (tipo VT \_ desconhecido) ou substitui um existente.<br/>                |
| [**Setiunknownvalue**](iportabledevicevalues-setiunknownvalue.md)                                                         | Adiciona um novo valor **IUnknown** (tipo VT \_ desconhecido) ou substitui um existente.<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | Adiciona um novo valor **PROPERTYKEY** (tipo VT \_ desconhecido) ou substitui um existente.<br/>                          |
| [**SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)                                               | Adiciona um novo valor **longo** (tipo VT \_ i4) ou substitui um existente.<br/>                                      |
| [**SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Adiciona um novo valor de **LONGLONG** (tipo VT \_ i8) ou substitui um existente.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Adiciona um novo valor de cadeia de caracteres (tipo VT \_ LPWSTR) ou substitui um existente.<br/>                                    |
| [**SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Adiciona um novo valor **ULONG** (tipo VT \_ UI4) ou substitui um existente.<br/>                                    |
| [**SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Adiciona um novo valor **ULONGLONG** (tipo VT \_ UI8) ou substitui um existente.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Adiciona um **novo valor PROPVARIANT** ou substitui um existente.<br/>                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces de coleção**](collection-interfaces.md)
</dt> </dl>

 

