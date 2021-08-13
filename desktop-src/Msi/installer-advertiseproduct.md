---
description: O método AdvertiseProduct do objeto do instalador anuncia um pacote de instalação.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Método Installer:: AdvertiseProduct'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a3792b279df9ac43fc09eaa02005cdaf3373e341bf2df40ce0a350d6c31bd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633285"
---
# <a name="installeradvertiseproduct-method"></a>Método Installer:: AdvertiseProduct

O método **AdvertiseProduct** do objeto do [**instalador**](installer-object.md) anuncia um pacote de instalação.

## <a name="syntax"></a>Sintaxe


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packagePath* 
</dt> <dd>

o caminho completo para o pacote de Windows Installer (.msi) a ser anunciado.

</dd> <dt>

*contexto* 
</dt> <dd>

O contexto do anúncio. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt> </dl> | Anuncia o aplicativo para uma [instalação no contexto de instalações](installation-context.md)por máquina. Isso torna o pacote disponível para instalação por todos os usuários do computador.<br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <dt>**msiAdvertiseProductUser**</dt> <dt>1</dt> </dl>             | Anuncia o aplicativo para uma instalação no [contexto de instalação](installation-context.md)por usuário.<br/>                                                                                   |



 

</dd> <dt>

*transformações* 
</dt> <dd>

A lista de transformações a ser aplicada ao produto. As transformações na lista são delimitadas por ponto e vírgula. Esse parâmetro é opcional.

</dd> <dt>

*linguagem* 
</dt> <dd>

O idioma do pacote de instalação a ser usado. Esse parâmetro é opcional.

</dd> <dt>

*options* 
</dt> <dd>

As opções de anúncio. Esse parâmetro é opcional. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | Anúncio padrão<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | Anuncia uma nova instância do produto. Requer que a primeira transformação na lista de transformação do parâmetro *transformações* seja a transformação de instância que altera o código do produto. Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **AdvertiseProduct** usa a função [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso do método **AdvertiseProduct** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 4,5 no Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




