---
description: A propriedade InstallProperty é o valor da propriedade da instância deste produto. Essa propriedade chama a função MsiGetProductInfoEx, com o ProductCode, userid e o contexto do objeto Product e a propriedade solicitada como um parâmetro.
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: Método Product. InstallProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.InstallProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12949997363fce8073c15f7ca6b7312c211fa0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751635"
---
# <a name="productinstallproperty-method"></a>Método Product. InstallProperty

A propriedade **InstallProperty** é o valor da propriedade da instância deste produto.

Essa propriedade chama a função [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) , com o *ProductCode*, *userid* e o *contexto* do objeto [**Product**](product-object.md) e a propriedade solicitada como um parâmetro.

## <a name="syntax"></a>Sintaxe


```JScript
Product.InstallProperty(
  property
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*property* 
</dt> <dd>

Especifica a propriedade a ser recuperada. As propriedades na lista a seguir só podem ser recuperadas de aplicativos que já estão instalados. Observe que as propriedades [necessárias](required-properties.md) têm garantia de disponibilidade, mas outras propriedades só estarão disponíveis se essa propriedade tiver sido definida. Consulte os links indicados para as [Propriedades](properties.md) do instalador para obter informações sobre como cada propriedade é definida.



| Propriedades instaladas                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**INSTALAR o \_ produtostate**</dt> </dl>                         | Estado do produto retornado na forma de cadeia de caracteres como "1" para anunciado e "5" para instalado.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**INSTALAR \_ HELPLINK**</dt> </dl>                                     | Link de suporte. Para obter mais informações, consulte a propriedade [**ARPHELPLINK**](arphelplink.md) .<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**INSTALAR \_ HELPTELEPHONE**</dt> </dl>                      | Telefone de suporte. Para obter mais informações, consulte a propriedade [**ARPHELPTELEPHONE**](arphelptelephone.md) .<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**INSTALAR \_ INSTALLDATE**</dt> </dl>                            | A última vez em que este produto recebeu o serviço. O valor dessa propriedade é substituído cada vez que um patch é aplicado ou removido do produto ou a opção de [linha de comando](command-line-options.md) /v é usada para reparar o produto. Se o produto não tiver recebido nenhum reparo ou patches, essa propriedade conterá a hora em que este produto foi instalado neste computador.<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**INSTALAR \_ INSTALLEDPRODUCTNAME**</dt> </dl> | Nome do produto instalado. Para obter mais informações, consulte a propriedade [**ProductName**](productname.md) .<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**INSTALAR \_ INSTALLLOCATION**</dt> </dl>                | Local de instalação. Para obter mais informações, consulte a propriedade [**ARPINSTALLLOCATION**](arpinstalllocation.md) .<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**Instalar o InstallException \_**</dt> </dl>                      | Origem da instalação. Para obter mais informações, consulte a propriedade [**SourceDir**](sourcedir.md) .<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**INSTALAR \_ LOCALPACKAGE**</dt> </dl>                         | Pacote armazenado em cache local.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**INSTALAR o \_ editorproperty**</dt> </dl>                                  | Editor. Para obter mais informações, consulte a propriedade [**fabricante**](manufacturer.md) .<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**INSTALAR \_ URLINFOABOUT**</dt> </dl>                         | Informações de URL. Para obter mais informações, consulte a propriedade [**ARPURLINFOABOUT**](arpurlinfoabout.md) .<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**INSTALAR \_ URLUPDATEINFO**</dt> </dl>                      | Informações de atualização de URL. Para obter mais informações, consulte a propriedade [**ARPURLUPDATEINFO**](arpurlupdateinfo.md) .<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**INSTALAR \_ VERSIONMINOR**</dt> </dl>                         | Versão secundária do produto derivada da propriedade [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**INSTALAR \_ Propriedade VersionMajor**</dt> </dl>                         | Versão principal do produto derivada da propriedade [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**INSTALAR \_ versãostring**</dt> </dl>                      | Versão do produto. Para obter mais informações, consulte a propriedade [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                    |



 

Para recuperar a ID do produto, o proprietário registrado ou a empresa registrada de aplicativos que já estão instalados, defina a *Propriedade* como um dos valores de cadeia de texto a seguir.



| Valor      | Descrição                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | O identificador do produto. Para obter mais informações, consulte a propriedade [**ProductID**](productid.md) . |
| RegCompany | A empresa se registrou para usar este produto.                                                    |
| RegOwner   | O proprietário registrado para usar este produto.                                                      |



 

Para recuperar o tipo de instância do produto, defina a *Propriedade* como o valor a seguir. Essa propriedade está disponível para produtos anunciados ou instalados.



| Valor        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstanceType | Um valor ausente ou um valor de 0 indica uma instalação normal do produto. Um valor de 1 indica um produto instalado usando uma transformação de várias instâncias e a propriedade [**MSINEWINSTANCE**](msinewinstance.md) . Disponível com o instalador que executa o Windows Server 2003 ou o Windows XP com SP1. Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md). |



 

As propriedades na lista a seguir também podem ser recuperadas de aplicativos que são anunciados. Essas propriedades não podem ser recuperadas para as instâncias de produto que são instaladas em um contexto por usuário-não gerenciado para contas de usuário que não sejam a conta de usuário atual.



| Propriedades anunciadas                 | Descrição                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| instalar \_ transformações           | Transformações.                                                                                                                                                                                                                                                                                          |
| idioma da instalação \_             | Idioma do produto.                                                                                                                                                                                                                                                                                    |
| INSTALAR o \_ NomeDoProduto          | Legível por humanos – nome do produto. Para obter mais informações, consulte a propriedade [**ProductName**](productname.md) .                                                                                                                                                                                              |
| de InstallProperty \_       | É igual a zero (0) se o produto for anunciado ou instalado por usuário. É igual a um (1) se o produto for anunciado ou instalado por computador para todos os usuários.<br/>                                                                                                                                  |
| INSTALAR \_ PACKAGECODE          | Identificador do pacote do qual este produto foi instalado. Para obter detalhes, consulte [códigos de pacote](package-codes.md).                                                                                                                                                                                      |
| versão de INSTALLproperty \_              | Versão do produto derivada da propriedade [**ProductVersion**](productversion.md) .                                                                                                                                                                                                                  |
| INSTALAR \_ PRODUCTICON          | Ícone principal do pacote. Para obter mais informações, consulte a propriedade [**ARPPRODUCTICON**](arpproducticon.md) .                                                                                                                                                                                       |
| INSTALAR \_ PackageName          | Nome do pacote de instalação original.                                                                                                                                                                                                                                                           |
| INSTALAR \_ \_ aplicativo lua autorizadoproperty \_ | Um valor de 1 indica um produto que pode ser atendido por não administradores usando a [aplicação de patch de UAC (controle de conta de usuário)](user-account-control--uac--patching.md). Um valor ausente ou um valor de 0 indica que a aplicação de patches com privilégios mínimos não está habilitada. Disponível com o Windows Installer 3,0 e posterior. |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a chamada for bem sucedido, a propriedade conterá o valor como uma cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Remessa**](product-object.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




